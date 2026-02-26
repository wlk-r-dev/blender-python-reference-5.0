# Audio System (aud)

Audaspace (pronounced “outer space”) is a high level audio library.

## Basic Sound Playback

This script shows how to use the classes: `Device`, `Sound` and `Handle`.
    
    
    import aud
    
    device = aud.Device()
    # Load sound file (it can be a video file with audio).
    sound = aud.Sound('music.ogg')
    
    # Play the audio, this return a handle to control play/pause.
    handle = device.play(sound)
    # If the audio is not too big and will be used often you can buffer it.
    sound_buffered = aud.Sound.cache(sound)
    handle_buffered = device.play(sound_buffered)
    
    # Stop the sounds (otherwise they play until their ends).
    handle.stop()
    handle_buffered.stop()
    

aud.AP_LOCATION
    

Constant value 3

aud.AP_ORIENTATION
    

Constant value 4

aud.AP_PANNING
    

Constant value 1

aud.AP_PITCH
    

Constant value 2

aud.AP_PITCH_SCALE
    

Constant value 6

aud.AP_TIME_STRETCH
    

Constant value 5

aud.AP_VOLUME
    

Constant value 0

aud.CHANNELS_INVALID
    

Constant value 0

aud.CHANNELS_MONO
    

Constant value 1

aud.CHANNELS_STEREO
    

Constant value 2

aud.CHANNELS_STEREO_LFE
    

Constant value 3

aud.CHANNELS_SURROUND4
    

Constant value 4

aud.CHANNELS_SURROUND5
    

Constant value 5

aud.CHANNELS_SURROUND51
    

Constant value 6

aud.CHANNELS_SURROUND61
    

Constant value 7

aud.CHANNELS_SURROUND71
    

Constant value 8

aud.CODEC_AAC
    

Constant value 1

aud.CODEC_AC3
    

Constant value 2

aud.CODEC_FLAC
    

Constant value 3

aud.CODEC_INVALID
    

Constant value 0

aud.CODEC_MP2
    

Constant value 4

aud.CODEC_MP3
    

Constant value 5

aud.CODEC_OPUS
    

Constant value 8

aud.CODEC_PCM
    

Constant value 6

aud.CODEC_VORBIS
    

Constant value 7

aud.CONTAINER_AAC
    

Constant value 8

aud.CONTAINER_AC3
    

Constant value 1

aud.CONTAINER_FLAC
    

Constant value 2

aud.CONTAINER_INVALID
    

Constant value 0

aud.CONTAINER_MATROSKA
    

Constant value 3

aud.CONTAINER_MP2
    

Constant value 4

aud.CONTAINER_MP3
    

Constant value 5

aud.CONTAINER_OGG
    

Constant value 6

aud.CONTAINER_WAV
    

Constant value 7

aud.DISTANCE_MODEL_EXPONENT
    

Constant value 5

aud.DISTANCE_MODEL_EXPONENT_CLAMPED
    

Constant value 6

aud.DISTANCE_MODEL_INVALID
    

Constant value 0

aud.DISTANCE_MODEL_INVERSE
    

Constant value 1

aud.DISTANCE_MODEL_INVERSE_CLAMPED
    

Constant value 2

aud.DISTANCE_MODEL_LINEAR
    

Constant value 3

aud.DISTANCE_MODEL_LINEAR_CLAMPED
    

Constant value 4

aud.FORMAT_FLOAT32
    

Constant value 36

aud.FORMAT_FLOAT64
    

Constant value 40

aud.FORMAT_INVALID
    

Constant value 0

aud.FORMAT_S16
    

Constant value 18

aud.FORMAT_S24
    

Constant value 19

aud.FORMAT_S32
    

Constant value 20

aud.FORMAT_U8
    

Constant value 1

aud.RATE_11025
    

Constant value 11025

aud.RATE_16000
    

Constant value 16000

aud.RATE_192000
    

Constant value 192000

aud.RATE_22050
    

Constant value 22050

aud.RATE_32000
    

Constant value 32000

aud.RATE_44100
    

Constant value 44100

aud.RATE_48000
    

Constant value 48000

aud.RATE_8000
    

Constant value 8000

aud.RATE_88200
    

Constant value 88200

aud.RATE_96000
    

Constant value 96000

aud.RATE_INVALID
    

Constant value 0

aud.STATUS_INVALID
    

Constant value 0

aud.STATUS_PAUSED
    

Constant value 2

aud.STATUS_PLAYING
    

Constant value 1

aud.STATUS_STOPPED
    

Constant value 3

aud.STRETCHER_QUALITY_CONSISTENT
    

Constant value 2

aud.STRETCHER_QUALITY_FAST
    

Constant value 1

aud.STRETCHER_QUALITY_HIGH
    

Constant value 0

_class _aud.AnimateableProperty
    

An AnimateableProperty object stores an array of float values for animating sound properties (e.g. pan, volume, pitch-scale)

read(_position_)
    

Reads the properties value at the given position.

Parameters:
    

**position** (_float_) – The position in the animation in frames.

Returns:
    

A numpy array of values representing the properties value.

Return type:
    

`numpy.ndarray`

readSingle(_position_)
    

Reads the properties value at the given position, assuming there is exactly one value.

Parameters:
    

**position** (_float_) – The position in the animation in frames.

Returns:
    

The value at that position.

Return type:
    

float

write(_data_[, _position_])
    

Writes the properties value.

If position is also given, the property is marked animated and the values are written starting at position.

Parameters:
    

  * **data** (_numpy.ndarray_) – numpy array of float32 values.

  * **position** (_int_) – The starting position in frames.


writeConstantRange(_data_ , _position_start_ , _position_end_)
    

Fills the properties frame range with a constant value and marks it animated.

Parameters:
    

  * **data** (_numpy.ndarray_) – numpy array of float values representing the constant value.

  * **position_start** (_int_) – The start position in frames.

  * **position_end** (_int_) – The end position in frames.


animated
    

Whether the property is animated.

count
    

The count of floats for a property.

_class _aud.Device
    

Device objects represent an audio output backend like OpenAL or SDL, but might also represent a file output or RAM buffer output.

lock()
    

Locks the device so that it’s guaranteed, that no samples are read from the streams until `unlock()` is called. This is useful if you want to do start/stop/pause/resume some sounds at the same time.

Note

The device has to be unlocked as often as locked to be able to continue playback.

Warning

Make sure the time between locking and unlocking is as short as possible to avoid clicks.

play(_sound_ , _keep =False_)
    

Plays a sound.

Parameters:
    

  * **sound** (`Sound`) – The sound to play.

  * **keep** (_bool_) – See `Handle.keep`.


Returns:
    

The playback handle with which playback can be controlled with.

Return type:
    

`Handle`

stopAll()
    

Stops all playing and paused sounds.

unlock()
    

Unlocks the device after a lock call, see `lock()` for details.

channels
    

The channel count of the device.

distance_model
    

The distance model of the device.

See also

[OpenAL Documentation](https://www.openal.org/documentation/)

doppler_factor
    

The doppler factor of the device. This factor is a scaling factor for the velocity vectors in doppler calculation. So a value bigger than 1 will exaggerate the effect as it raises the velocity.

format
    

The native sample format of the device.

listener_location
    

The listeners’s location in 3D space, a 3D tuple of floats.

listener_orientation
    

The listener’s orientation in 3D space as quaternion, a 4 float tuple.

listener_velocity
    

The listener’s velocity in 3D space, a 3D tuple of floats.

rate
    

The sampling rate of the device in Hz.

speed_of_sound
    

The speed of sound of the device. The speed of sound in air is typically 343.3 m/s.

volume
    

The overall volume of the device.

_class _aud.DynamicMusic
    

The DynamicMusic object allows to play music depending on a current scene, scene changes are managed by the class, with the possibility of custom transitions. The default transition is a crossfade effect, and the default scene is silent and has id 0

addScene(_scene_)
    

Adds a new scene.

Parameters:
    

**scene** (`Sound`) – The scene sound.

Returns:
    

The new scene id.

Return type:
    

int

addTransition(_ini_ , _end_ , _transition_)
    

Adds a new scene.

Parameters:
    

  * **ini** (_int_) – the initial scene foor the transition.

  * **end** (_int_) – The final scene for the transition.

  * **transition** (`Sound`) – The transition sound.


Returns:
    

false if the ini or end scenes don’t exist, true otherwise.

Return type:
    

bool

pause()
    

Pauses playback of the scene.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

resume()
    

Resumes playback of the scene.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

stop()
    

Stops playback of the scene.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

fadeTime
    

The length in seconds of the crossfade transition

position
    

The playback position of the scene in seconds.

scene
    

The current scene

status
    

Whether the scene is playing, paused or stopped (=invalid).

volume
    

The volume of the scene.

_class _aud.HRTF
    

An HRTF object represents a set of head related transfer functions as impulse responses. It’s used for binaural sound

loadLeftHrtfSet(_extension_ , _directory_)
    

Loads all HRTFs from a directory.

Parameters:
    

  * **extension** (_string_) – The file extension of the hrtfs.

  * **directory** – The path to where the HRTF files are located.


Returns:
    

The loaded `HRTF` object.

Return type:
    

`HRTF`

loadRightHrtfSet(_extension_ , _directory_)
    

Loads all HRTFs from a directory.

Parameters:
    

  * **extension** (_string_) – The file extension of the hrtfs.

  * **directory** – The path to where the HRTF files are located.


Returns:
    

The loaded `HRTF` object.

Return type:
    

`HRTF`

addImpulseResponseFromSound(_sound_ , _azimuth_ , _elevation_)
    

Adds a new hrtf to the HRTF object

Parameters:
    

  * **sound** (`Sound`) – The sound that contains the hrtf.

  * **azimuth** (_float_) – The azimuth angle of the hrtf.

  * **elevation** (_float_) – The elevation angle of the hrtf.


Returns:
    

Whether the action succeeded.

Return type:
    

bool

_class _aud.Handle
    

Handle objects are playback handles that can be used to control playback of a sound. If a sound is played back multiple times then there are as many handles.

pause()
    

Pauses playback.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

resume()
    

Resumes playback.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

stop()
    

Stops playback.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

Note

This makes the handle invalid.

attenuation
    

This factor is used for distance based attenuation of the source.

See also

`Device.distance_model`

cone_angle_inner
    

The opening angle of the inner cone of the source. If the cone values of a source are set there are two (audible) cones with the apex at the `location` of the source and with infinite height, heading in the direction of the source’s `orientation`. In the inner cone the volume is normal. Outside the outer cone the volume will be `cone_volume_outer` and in the area between the volume will be interpolated linearly.

cone_angle_outer
    

The opening angle of the outer cone of the source.

See also

`cone_angle_inner`

cone_volume_outer
    

The volume outside the outer cone of the source.

See also

`cone_angle_inner`

distance_maximum
    

The maximum distance of the source. If the listener is further away the source volume will be 0.

See also

`Device.distance_model`

distance_reference
    

The reference distance of the source. At this distance the volume will be exactly `volume`.

See also

`Device.distance_model`

keep
    

Whether the sound should be kept paused in the device when its end is reached. This can be used to seek the sound to some position and start playback again.

Warning

If this is set to true and you forget stopping this equals a memory leak as the handle exists until the device is destroyed.

location
    

The source’s location in 3D space, a 3D tuple of floats.

loop_count
    

The (remaining) loop count of the sound. A negative value indicates infinity.

orientation
    

The source’s orientation in 3D space as quaternion, a 4 float tuple.

pitch
    

The pitch of the sound.

position
    

The playback position of the sound in seconds.

relative
    

Whether the source’s location, velocity and orientation is relative or absolute to the listener.

status
    

Whether the sound is playing, paused or stopped (=invalid).

velocity
    

The source’s velocity in 3D space, a 3D tuple of floats.

volume
    

The volume of the sound.

volume_maximum
    

The maximum volume of the source.

See also

`Device.distance_model`

volume_minimum
    

The minimum volume of the source.

See also

`Device.distance_model`

_class _aud.ImpulseResponse
    

An ImpulseResponse object represents a filter with which to convolve a sound.

_class _aud.PlaybackManager
    

A PlabackManager object allows to easily control groups os sounds organized in categories.

addCategory(_volume_)
    

Adds a category with a custom volume.

Parameters:
    

**volume** (_float_) – The volume for ther new category.

Returns:
    

The key of the new category.

Return type:
    

int

clean()
    

Cleans all the invalid and finished sound from the playback manager.

getVolume(_catKey_)
    

Retrieves the volume of a category.

Parameters:
    

**catKey** (_int_) – the key of the category.

Returns:
    

The volume of the category.

Return type:
    

float

pause(_catKey_)
    

Pauses playback of the category.

Parameters:
    

**catKey** (_int_) – the key of the category.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

play(_sound_ , _catKey_)
    

Plays a sound through the playback manager and assigns it to a category.

Parameters:
    

  * **sound** (`Sound`) – The sound to play.

  * **catKey** (_int_) – the key of the category in which the sound will be added, if it doesn’t exist, a new one will be created.


Returns:
    

The playback handle with which playback can be controlled with.

Return type:
    

`Handle`

resume(_catKey_)
    

Resumes playback of the catgory.

Parameters:
    

**catKey** (_int_) – the key of the category.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

setVolume(_volume_ , _catKey_)
    

Changes the volume of a category.

Parameters:
    

  * **volume** (_float_) – the new volume value.

  * **catKey** (_int_) – the key of the category.


Returns:
    

Whether the action succeeded.

Return type:
    

int

stop(_catKey_)
    

Stops playback of the category.

Parameters:
    

**catKey** (_int_) – the key of the category.

Returns:
    

Whether the action succeeded.

Return type:
    

bool

_class _aud.Sequence
    

This sound represents sequenced entries to play a sound sequence.

add()
    

Adds a new entry to the sequence.

Parameters:
    

  * **sound** (`Sound`) – The sound this entry should play.

  * **begin** (_double_) – The start time.

  * **end** (_double_) – The end time or a negative value if determined by the sound.

  * **skip** (_double_) – How much seconds should be skipped at the beginning.


Returns:
    

The entry added.

Return type:
    

`SequenceEntry`

remove()
    

Removes an entry from the sequence.

Parameters:
    

**entry** (`SequenceEntry`) – The entry to remove.

setAnimationData()
    

Writes animation data to a sequence.

Parameters:
    

  * **type** (_int_) – The type of animation data.

  * **frame** (_int_) – The frame this data is for.

  * **data** (_sequence_ _of_ _float_) – The data to write.

  * **animated** (_bool_) – Whether the attribute is animated.


channels
    

The channel count of the sequence.

distance_model
    

The distance model of the sequence.

See also

[OpenAL Documentation](https://www.openal.org/documentation/)

doppler_factor
    

The doppler factor of the sequence. This factor is a scaling factor for the velocity vectors in doppler calculation. So a value bigger than 1 will exaggerate the effect as it raises the velocity.

fps
    

The listeners’s location in 3D space, a 3D tuple of floats.

muted
    

Whether the whole sequence is muted.

rate
    

The sampling rate of the sequence in Hz.

speed_of_sound
    

The speed of sound of the sequence. The speed of sound in air is typically 343.3 m/s.

_class _aud.SequenceEntry
    

SequenceEntry objects represent an entry of a sequenced sound.

move()
    

Moves the entry.

Parameters:
    

  * **begin** (_double_) – The new start time.

  * **end** (_double_) – The new end time or a negative value if unknown.

  * **skip** (_double_) – How many seconds to skip at the beginning.


setAnimationData()
    

Writes animation data to a sequenced entry.

Parameters:
    

  * **type** (_int_) – The type of animation data.

  * **frame** (_int_) – The frame this data is for.

  * **data** (_sequence_ _of_ _float_) – The data to write.

  * **animated** (_bool_) – Whether the attribute is animated.


attenuation
    

This factor is used for distance based attenuation of the source.

See also

`Device.distance_model`

cone_angle_inner
    

The opening angle of the inner cone of the source. If the cone values of a source are set there are two (audible) cones with the apex at the `location` of the source and with infinite height, heading in the direction of the source’s `orientation`. In the inner cone the volume is normal. Outside the outer cone the volume will be `cone_volume_outer` and in the area between the volume will be interpolated linearly.

cone_angle_outer
    

The opening angle of the outer cone of the source.

See also

`cone_angle_inner`

cone_volume_outer
    

The volume outside the outer cone of the source.

See also

`cone_angle_inner`

distance_maximum
    

The maximum distance of the source. If the listener is further away the source volume will be 0.

See also

`Device.distance_model`

distance_reference
    

The reference distance of the source. At this distance the volume will be exactly `volume`.

See also

`Device.distance_model`

muted
    

Whether the entry is muted.

relative
    

Whether the source’s location, velocity and orientation is relative or absolute to the listener.

sound
    

The sound the entry is representing and will be played in the sequence.

volume_maximum
    

The maximum volume of the source.

See also

`Device.distance_model`

volume_minimum
    

The minimum volume of the source.

See also

`Device.distance_model`

_class _aud.Sound
    

Sound objects are immutable and represent a sound that can be played simultaneously multiple times. They are called factories because they create reader objects internally that are used for playback.

_classmethod _buffer(_data_ , _rate_)
    

Creates a sound from a data buffer.

Parameters:
    

  * **data** (`numpy.ndarray`) – The data as two dimensional numpy array.

  * **rate** (_double_) – The sample rate.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

_classmethod _file(_filename_)
    

Creates a sound object of a sound file.

Parameters:
    

**filename** (_string_) – Path of the file.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Warning

If the file doesn’t exist or can’t be read you will not get an exception immediately, but when you try to start playback of that sound.

_classmethod _list()
    

Creates an empty sound list that can contain several sounds.

Parameters:
    

**random** (_int_) – whether the playback will be random or not.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

_classmethod _sawtooth(_frequency_ , _rate =48000_)
    

Creates a sawtooth sound which plays a sawtooth wave.

Parameters:
    

  * **frequency** (_float_) – The frequency of the sawtooth wave in Hz.

  * **rate** (_int_) – The sampling rate in Hz. It’s recommended to set this value to the playback device’s sampling rate to avoid resampling.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

_classmethod _silence(_rate =48000_)
    

Creates a silence sound which plays simple silence.

Parameters:
    

**rate** (_int_) – The sampling rate in Hz. It’s recommended to set this value to the playback device’s sampling rate to avoid resampling.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

_classmethod _sine(_frequency_ , _rate =48000_)
    

Creates a sine sound which plays a sine wave.

Parameters:
    

  * **frequency** (_float_) – The frequency of the sine wave in Hz.

  * **rate** (_int_) – The sampling rate in Hz. It’s recommended to set this value to the playback device’s sampling rate to avoid resampling.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

_classmethod _square(_frequency_ , _rate =48000_)
    

Creates a square sound which plays a square wave.

Parameters:
    

  * **frequency** (_float_) – The frequency of the square wave in Hz.

  * **rate** (_int_) – The sampling rate in Hz. It’s recommended to set this value to the playback device’s sampling rate to avoid resampling.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

_classmethod _triangle(_frequency_ , _rate =48000_)
    

Creates a triangle sound which plays a triangle wave.

Parameters:
    

  * **frequency** (_float_) – The frequency of the triangle wave in Hz.

  * **rate** (_int_) – The sampling rate in Hz. It’s recommended to set this value to the playback device’s sampling rate to avoid resampling.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

ADSR(_attack_ , _decay_ , _sustain_ , _release_)
    

Attack-Decay-Sustain-Release envelopes the volume of a sound. Note: there is currently no way to trigger the release with this API.

Parameters:
    

  * **attack** (_float_) – The attack time in seconds.

  * **decay** (_float_) – The decay time in seconds.

  * **sustain** (_float_) – The sustain level.

  * **release** (_float_) – The release level.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

accumulate(_additive =False_)
    

Accumulates a sound by summing over positive input differences thus generating a monotonic sigal. If additivity is set to true negative input differences get added too, but positive ones with a factor of two.

Note that with additivity the signal is not monotonic anymore.

Parameters:
    

**additive** – Whether the accumulation should be additive or not.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

addSound(_sound_)
    

Adds a new sound to a sound list.

Parameters:
    

**sound** (`Sound`) – The sound that will be added to the list.

Note

You can only add a sound to a sound list.

animateableTimeStretchPitchScale(_fps_[, _time_stretch_ , _pitch_scale_ , _quality_ , _preserve_formant_])
    

Applies time-stretching and pitch-scaling to the sound.

Parameters:
    

  * **fps** (_float_) – The FPS of the animation system.

  * **time_stretch** (float or `AnimateablePropertyP`) – The factor by which to stretch or compress time.

  * **pitch_scale** (float or `AnimateablePropertyP` :arg quality: Rubberband stretcher quality (STRETCHER_QUALITY_*).) – The factor by which to adjust the pitch.

  * **preserve_formant** (_bool_) – Whether to preserve the vocal formants during pitch-shifting.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

binaural()
    

Creates a binaural sound using another sound as source. The original sound must be mono

Parameters:
    

  * **hrtfs** – An HRTF set.

  * **source** (`Source`) – An object representing the source position of the sound.

  * **threadPool** (`ThreadPool`) – A thread pool used to parallelize convolution.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

cache()
    

Caches a sound into RAM.

This saves CPU usage needed for decoding and file access if the underlying sound reads from a file on the harddisk, but it consumes a lot of memory.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

Only known-length factories can be buffered.

Warning

Raw PCM data needs a lot of space, only buffer short factories.

convolver()
    

Creates a sound that will apply convolution to another sound.

Parameters:
    

  * **impulseResponse** (`ImpulseResponse`) – The filter with which convolve the sound.

  * **threadPool** (`ThreadPool`) – A thread pool used to parallelize convolution.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

data()
    

Retrieves the data of the sound as numpy array.

Returns:
    

A two dimensional numpy float array.

Return type:
    

`numpy.ndarray`

Note

Best efficiency with cached sounds.

delay(_time_)
    

Delays by playing adding silence in front of the other sound’s data.

Parameters:
    

**time** (_float_) – How many seconds of silence should be added before the sound.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

envelope(_attack_ , _release_ , _threshold_ , _arthreshold_)
    

Delays by playing adding silence in front of the other sound’s data.

Parameters:
    

  * **attack** (_float_) – The attack factor.

  * **release** (_float_) – The release factor.

  * **threshold** (_float_) – The general threshold value.

  * **arthreshold** (_float_) – The attack/release threshold value.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

fadein(_start_ , _length_)
    

Fades a sound in by raising the volume linearly in the given time interval.

Parameters:
    

  * **start** (_float_) – Time in seconds when the fading should start.

  * **length** (_float_) – Time in seconds how long the fading should last.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

Before the fade starts it plays silence.

fadeout(_start_ , _length_)
    

Fades a sound in by lowering the volume linearly in the given time interval.

Parameters:
    

  * **start** (_float_) – Time in seconds when the fading should start.

  * **length** (_float_) – Time in seconds how long the fading should last.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

After the fade this sound plays silence, so that the length of the sound is not altered.

filter(_b_ , _a =(1,)_)
    

Filters a sound with the supplied IIR filter coefficients. Without the second parameter you’ll get a FIR filter.

If the first value of the a sequence is 0, it will be set to 1 automatically. If the first value of the a sequence is neither 0 nor 1, all filter coefficients will be scaled by this value so that it is 1 in the end, you don’t have to scale yourself.

Parameters:
    

  * **b** (_sequence_ _of_ _float_) – The nominator filter coefficients.

  * **a** (_sequence_ _of_ _float_) – The denominator filter coefficients.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

highpass(_frequency_ , _Q =0.5_)
    

Creates a second order highpass filter based on the transfer function \\(H(s) = s^2 / (s^2 + s/Q + 1)\\)

Parameters:
    

  * **frequency** (_float_) – The cut off trequency of the highpass.

  * **Q** (_float_) – Q factor of the lowpass.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

join(_sound_)
    

Plays two factories in sequence.

Parameters:
    

**sound** (`Sound`) – The sound to play second.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

The two factories have to have the same specifications (channels and samplerate).

limit(_start_ , _end_)
    

Limits a sound within a specific start and end time.

Parameters:
    

  * **start** (_float_) – Start time in seconds.

  * **end** (_float_) – End time in seconds.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

loop(_count_)
    

Loops a sound.

Parameters:
    

**count** (_integer_) – How often the sound should be looped. Negative values mean endlessly.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

This is a filter function, you might consider using `Handle.loop_count` instead.

lowpass(_frequency_ , _Q =0.5_)
    

Creates a second order lowpass filter based on the transfer function \\(H(s) = 1 / (s^2 + s/Q + 1)\\)

Parameters:
    

  * **frequency** (_float_) – The cut off trequency of the lowpass.

  * **Q** (_float_) – Q factor of the lowpass.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

mix(_sound_)
    

Mixes two factories.

Parameters:
    

**sound** (`Sound`) – The sound to mix over the other.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

The two factories have to have the same specifications (channels and samplerate).

modulate(_sound_)
    

Modulates two factories.

Parameters:
    

**sound** (`Sound`) – The sound to modulate over the other.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

The two factories have to have the same specifications (channels and samplerate).

mutable()
    

Creates a sound that will be restarted when sought backwards. If the original sound is a sound list, the playing sound can change.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

pingpong()
    

Plays a sound forward and then backward. This is like joining a sound with its reverse.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

pitch(_factor_)
    

Changes the pitch of a sound with a specific factor.

Parameters:
    

**factor** (_float_) – The factor to change the pitch with.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

This is done by changing the sample rate of the underlying sound, which has to be an integer, so the factor value rounded and the factor may not be 100 % accurate.

Note

This is a filter function, you might consider using `Handle.pitch` instead.

rechannel(_channels_)
    

Rechannels the sound.

Parameters:
    

**channels** (_int_) – The new channel configuration.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

resample(_rate_ , _quality_)
    

Resamples the sound.

Parameters:
    

  * **rate** (_double_) – The new sample rate.

  * **quality** (_int_) – Resampler performance vs quality choice (0=fastest, 3=slowest).


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

reverse()
    

Plays a sound reversed.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

The sound has to have a finite length and has to be seekable. It’s recommended to use this only with factories with fast and accurate seeking, which is not true for encoded audio files, such ones should be buffered using `cache()` before being played reversed.

Warning

If seeking is not accurate in the underlying sound you’ll likely hear skips/jumps/cracks.

sum()
    

Sums the samples of a sound.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

threshold(_threshold =0_)
    

Makes a threshold wave out of an audio wave by setting all samples with a amplitude >= threshold to 1, all <= -threshold to -1 and all between to 0.

Parameters:
    

**threshold** (_float_) – Threshold value over which an amplitude counts non-zero.

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

timeStretchPitchScale(_time_stretch_ , _pitch_scale_ , _quality_ , _preserve_formant_)
    

Applies time-stretching and pitch-scaling to the sound.

Parameters:
    

  * **time_stretch** (_float_) – The factor by which to stretch or compress time.

  * **pitch_scale** (_float_) – The factor by which to adjust the pitch.

  * **quality** (_int_) – Rubberband stretcher quality (STRETCHER_QUALITY_*).

  * **preserve_formant** (_bool_) – Whether to preserve the vocal formants during pitch-shifting.


Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

volume(_volume_)
    

Changes the volume of a sound.

Parameters:
    

**volume** (_float_) – The new volume..

Returns:
    

The created `Sound` object.

Return type:
    

`Sound`

Note

Should be in the range [0, 1] to avoid clipping.

Note

This is a filter function, you might consider using `Handle.volume` instead.

write(_filename_ , _rate_ , _channels_ , _format_ , _container_ , _codec_ , _bitrate_ , _buffersize_)
    

Writes the sound to a file.

Parameters:
    

  * **filename** (_string_) – The path to write to.

  * **rate** (_int_) – The sample rate to write with.

  * **channels** (_int_) – The number of channels to write with.

  * **format** (_int_) – The sample format to write with.

  * **container** (_int_) – The container format for the file.

  * **codec** (_int_) – The codec to use in the file.

  * **bitrate** (_int_) – The bitrate to write with.

  * **buffersize** (_int_) – The size of the writing buffer.


length
    

The sample specification of the sound as a tuple with rate and channel count.

specs
    

The sample specification of the sound as a tuple with rate and channel count.

_class _aud.Source
    

The source object represents the source position of a binaural sound.

azimuth
    

The azimuth angle.

distance
    

The distance value. 0 is min, 1 is max.

elevation
    

The elevation angle.

_class _aud.ThreadPool
    

A ThreadPool is used to parallelize convolution efficiently.

_class _aud.error

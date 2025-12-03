# drumbuster-PD
for use with PureData Vanilla v.0.55.2. This is a drum machine and synthesizer that allows four samples to be loaded and triggered using a 16 step sequencer. With each trigger, the sample becomes "corrupted," gradually introducing a glitchy, harsh timbre.

IMPORTANT: Always be wary of volume when using PureData! Start low, and then move high. Volume levels can quickly become a hazard to health if caution is not exercised.

Startup instructions:

1. Ensure PureData v.0.55.2 has been installed prior to use. PureData can be downloaded for free from Miller Puckette's website: https://puredata.info/
2. Ensure your audio outputs are configured correctly and your DSP (located under the "media" tab in the ribbon) is toggled to the "On" position.
3. Upon opening the patch, you may use the small white buttons (or "bangs") below the drumbusterArrays to open a file-loading panel. From here, select up to four audio samples. MSC-DL-909 drum machine samples are included in the main branch. NOTE: drumbuster functions best with samples no longer than a couple of seconds.

Drum Sequencer:
There are 4 16-step sequencers that correspond to each of the drumbusterArray samples. By clicking the white squares, you can create rhythmic patterns. You can click and drag the number box to the right of the sequencers to enter your BPM information. To start the drum sequencer, click the green "start" button. To stop it, click the red "stop" button. Presets: (16s - every 16th note; 8s - every 8th note; I 8s - every other 8th note; 4s - four on the floor; CLEAR - clears the pattern; unlabelled - random sequence.)

Synthesizer:
This sample-and-hold downsampling synthesizer was entirely constructed by Simon Hutchinson (https://www.youtube.com/watch?v=QfLJujXbeh0). To use it, click and drag the two sliders below "synthSequence" into the audio range. Create a sequence by clicking and dragging your mouse across the array. When you're ready, click the green "start" button and slowly increase the volume. The "random alias" button will randomly cycle through alias values.

Buster:
Click and drag the "corruption size" slider to select how large a collection of audio samples you'd like to process per trigger of the corresponding drumbusterArray. The larger the sample, the more computationally expensive the trigger will be - be mindful not to "overkill," which may compromise the stability of the patch. 
Similarly, "corruption lvl" sets the numeric amount that will be added or subtracted from the drumbusterArray. A low level will result in subtle changes, while a high level will create very large spikes in the waveform.
The "linear/random" switch selects between two modes. In "linear" mode, the corruptions proceed one after the other until they reach the end of the audio file, at which point they circle back to the front. In "random" mode, a random starting point is chosen somewhere in the file.
By default, the samples are set to play uncorrupted. To begin corruption, click the "allow corruption" button for the corresponding file. If you want all four samples to be available for corruption, click the "global corrupt" toggle on the right hand side of the box. To reset the audio files to their base state, click "reset sample."

Stereo Savefile:
To save a performance, first click the "OPENFILE" button. Name your file, press OK, and then click the red "REC" box so that an X appears. You are now recording. When you would like to stop the recording, press the "REC" box again. The X will disappear, and your named .wav file will appear in the main PureData file directory.

This software is free to use, modify and distribute. Have fun making music!

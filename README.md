# Generate Digit Dataset (GDD)

A simple audio/speech dataset consisting of recordings of spoken digits in `wav` files at 8kHz. The recordings are trimmed so that they have near minimal silence at the beginnings and ends.

GDD is an open dataset, which means it will grow over time as data is contributed.

### Current status
- 6 speakers
- 3,000 recordings (50 of each digit per speaker)
- English pronunciations

### Organization
Files are named in the following format:
`{digitLabel}_{speakerName}_{index}.wav`
Example: `7_anjul_32.wav`

### Contributions
Please contribute your homemade recordings. All recordings should be mono 8kHz `wav ` files and be trimmed to have minimal silence. Don't forget to update `metadata.py` with the speaker meta-data.

To add your data, follow the recording instructions in `acquire_data/say_numbers_prompt.py`
and then run `split_and_label_numbers.py` to make your files.

### Metadata
`metadata.py` contains meta-data regarding the speakers gender and accents.

### Included utilities
`trimmer.py`
Trims silences at beginning and end of an audio file. Splits an audio file into multiple audio files by periods of silence.

`fsdd.py`
A simple class that provides an easy to use API to access the data.

`spectogramer.py`
Used for creating spectrograms of the audio data. Spectrograms are often a useful pre-processing step.

### Usage
The test set officially consists of the first 10% of the recordings. Recordings numbered `0-4` (inclusive) are in the test and `5-49` are in the training set.

### Converting speech to text using Mozilla Deepspeech

- Install `Deepspeech` using `pip install deepspeech`
- Clone the [Deepspeech-example](https://github.com/mozilla/DeepSpeech-examples/tree/r0.9) repository
- We are going to use the `vad_transcriber`. The code will be executed from here.
- Execute the command `sudo apt install sox` to install Sound eXchange (sox)
- Setup the environment,
  - `sudo apt install virtualenv`
  - `cd examples/vad_transcriber`
  - `virtualenv -p python3 venv`
  - `source venv/bin/activate`
  - `pip3 install -r requirements.txt`
- Create a folder called `models` and download the model files using,

    `curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.pbmm`
    
    `curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.scorer`
- Convert the audio file in wav format
- Use the command `python3 audioTranscript_cmd.py --aggressive 1 --audio audio_file_location --model ./models/` to convert

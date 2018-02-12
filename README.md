__Simple set of scripts to synthesise single words (or non-words)
from a .txt file, and save them as .wav files__

__ Example: __

```python
# modules
from synthesise_word_list import synthesise_word_wav

# directories
word_list_file = 'my_word_list.txt'
save_dir = 'where_to_save_files'

# params
speaker = 'Samantha'
speech_rate = 150

with open(word_list_file) as f:
    
    # load file as list
    words = f.read().splitlines()

    # loop through each word and save
    for word in words:
		synthesise_word_wav(word, speaker, save_dir, speech_rate)
```
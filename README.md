
# NeuralCharTransliteration
Neural Transliteration of Song Lyrics (Roman to Hindi Script)<br />
with current model 83.43% on test file<br />

# Data/Input-Output
Web scapped Hindi song lyrics<br />
train and test file format: one word pair per line, english_word<tab>hindi_word, blank_line = end_of_sentence<br />
training file = train_file.txt <br />
test file = test_file.txt<br />
output file = test.txt.out<br />
output file format: tab separated triple, english_word<tab>gold_hi_word<tab>pred_hi_word, blank_line = end_of_sentence<br />
  
 # Requirement
 1. python 3<br />
 2. tensorflow 1.0.1<br />
 3. keras 2.0.2<br />
 4. numpy 1.12.1<br />

# model
input = en_chr_idx<br />
embedding <- en_chr_idx<br />
bi-LSTM <- embedding<br />
output <- timedistributed_dense(hi_char_len, softmax) <- bi-LSTM<br />

# traning/tesing
please view NCT.py

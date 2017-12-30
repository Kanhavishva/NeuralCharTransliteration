
# NeuralCharTransliteration
Neural Transliteration of Song Lyrics (Roman to Hindi Script)
with current model 83.43% on test file

# Data/Input-Output
Web scapped Hindi song lyrics
train and test file format: one word pair per line, english_word<tab>hindi_word, blank_line = end_of_sentence
training file = train_file.txt 
test file = test_file.txt
output file = test.txt.out
output file format: tab separated triple, english_word<tab>gold_hi_word<tab>pred_hi_word, blank_line = end_of_sentence
  
 # Requirement
 1. python 3
 2. tensorflow 1.0.1
 3. keras 2.0.2
 4. numpy 1.12.1

# model
input = en_chr_idx
embedding <- en_chr_idx
bi-LSTM <- embedding
output <- timedistributed_dense(hi_char_len, softmax) <- bi-LSTM

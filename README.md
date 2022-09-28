# asm-pos
# Asamese POS- Pre-trained model for Assamese POS tagging

This repository contains two pre-trained models for Assamese POS tagging- 

1) Stacked embedding (MuRIL + Word2vec) method is used to embed the sentence for training. It achieved F1-score of 74.46% in tagging. The link to the model-[Download](https://drive.google.com/file/d/1LAi6cZMyRFWoB6uYIWp3CPtTTnfnOCfx/view?usp=sharing)
2) Stacked embedding (MuRIL + FlairEmbedding) method is used to embed the sentence for training. It achieves F1-score of 74.62% in POS tagging. The link to the model- [Download](https://drive.google.com/file/d/1MC7mVOguotsPEnpLiL20ag97O7siMqvU/view?usp=sharing)

Assamese Monolingual Text Corpus ILCI-II which is acquired form TDIL to train the model. 

## How to run

Download the pre-trained model from the [link](https://drive.google.com/file/d/1QGR0zlf4adfxPRJwStbHyNPfpu4upWf7/view?usp=sharing)

```
from flair.models import SequenceTagger
from flair.data import  Sentence, Token

# Load the tagger


model = SequenceTagger.load('AsPOS.pt') 

#  create example sentence
sen='ভাৰতীয় পেচ বলাৰ জৱাগল শ্রীনাথে আক্রমণ কৰিবলৈ আৰম্ভ কৰি প্রথম বলটোতেই শ্রীলংকাপেনাৰ ৰমেশ কালুৱিথার্ণাক পেভিলিয়নলৈ পঠিয়াইছিল ৷'
sentence = Sentence(sen)

# predict tags and print
model.predict(sentence)
print(sentence.to_tagged_string())

```

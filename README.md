# asm-pos
# Pre-trained model for Assamese POS tagging using Flair

This repository contains pre-trained model for Assamese POS tagging based on Flair framework. We used Assamese Monolingual Text Corpus ILCI-II acquired form TDIL to train the model. The accuracy of the model is 71.87%

## How to run

Download the pre-trained model from the link- https://drive.google.com/file/d/1QGR0zlf4adfxPRJwStbHyNPfpu4upWf7/view?usp=sharing

```
from flair.models import SequenceTagger
from flair.data import  Sentence, Token

# Load the tagger

model = SequenceTagger.load('final-model.pt')

#  create example sentence
sen='ভাৰতীয় পেচ বলাৰ জৱাগল শ্রীনাথে আক্রমণ কৰিবলৈ আৰম্ভ কৰি প্রথম বলটোতেই শ্রীলংকাপেনাৰ ৰমেশ কালুৱিথার্ণাক পেভিলিয়নলৈ পঠিয়াইছিল ৷'
sentence = Sentence(sen)

# predict tags and print
model.predict(sentence)
print(sentence.to_tagged_string())

```

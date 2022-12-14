# anti-cursing

**"anti-cursing"** is a python package that detects and switches negative or any kind of cursing word from sentences or comments whatever๐คฌ

You just install the package the way you install any other package and then you can use it in your code.

So this is __**the very first idea**__

But you can find my package in pypi(https://pypi.org/project/anti-cursing/0.0.2/)

**๐๐ปPlz bare with the program to install model's weight and bias from huggingface at the first time you use the package.**

<img width="1134" alt="image" src="https://user-images.githubusercontent.com/50198431/203723736-3aeb84a1-6418-4190-b967-2888e14b14fd.png">

<hr>

# Concept
There are often situations where you have to code something, detect a forbidden word, and change it to another word.
Hardcoding all parts is very inconvenient, and in the Python ecosystem, there are many packages to address.
One of them is **"anti-cursing"**.

The package, which operates exclusively for **Korean**, does not simply change the banned word by setting it up, but detects and replaces the banned word by learning a deep learning model.

Therefore, it is easy to cope with new malicious words as long as they are learned.
For this purpose, semi-supervied learning through pseudo labeling is used.

Additionally, instead of changing malicious words to special characters such as --- or ***, you can convert them into emojis to make them more natural.

# Contents

- [Installation](#installation)
- [Usage](#usage)
- [Model comparison](#model-comparison)
- [Dataset](#dataset)
- [Used API](#used-api)
- [License](#license)
- [References](#references)
- [Project Status](#project-status)
- [Future Work](#future-work)


# Installation

You can install the package using pip:

```bash
pip install anti-cursing
```

https://user-images.githubusercontent.com/50198431/204080173-6542f90c-ff37-4fe0-bfe3-b82620b02274.mp4

# Usage

```python
from anti_cursing.utils import antiCursing

antiCursing.anti_cur("๋๋ ๋๊ฐ ์ข์ง๋ง, ๋๋ ๋๋ฌด ๊ฐ์๋ผ์ผ")
```

```bash
๋๋ ๋๊ฐ ์ข์ง๋ง, ๋๋ ๋๋ฌด ๐ผ๐ป์ผ
```

https://user-images.githubusercontent.com/50198431/204080186-6ba66d00-b076-4256-9c0d-32120740ffcb.mp4

# Model-comparison
| Classification | KcElectra | KoBERT | RoBERTa-base | RoBERTa-large |
| --- | --- | --- | --- | --- |
| Validation Accuracy | 0.88680 | 0.85721 | 0.83421 | 0.86994 |
| Validation Loss | 1.00431 | 1.23237 | 1.30012 | 1.16179 |
| Training Loss | 0.09908 | 0.03761 | 0.0039 | 0.06255 |
| Epoch | 10 | 40 | 20 | 20 |
| Batch-size | 8 | 32 | 16 | 32 |
| transformers | beomi/KcELECTRA-base | skt/kobert-base-v1 | xlm-roberta-base | klue/roberta-large |

# Dataset
* ### Smilegate-AI 
  * https://github.com/smilegate-ai/korean_unsmile_dataset
  * Korean Sentiment Analysis
  * [paper](#korean-unsmile-dataset)
* ### Naver portal news articles crawling
  * https://news.naver.com
  * Non-labeled Data for Test Dataset
* ### ๐ Emoji unicode crawling for encoding
  * https://unicode.org/emoji/charts/full-emoji-list.html

# Used-api
### Google translator
* https://cloud.google.com/translate/docs (API DOCS)

# License

This repository is licensed under the MIT license. See LICENSE for details.

Click here to see the License information --> [License](LICENSE)

# References

### Sentiment Analysis Based on Deep Learning : A Comparative Study
  * Nhan Cach Dang, Maria N. Moreno-Garcia, Fernando De la Prieta. 2006. Sentiment Analysis Based on Deep Learning : A Comparative Study. In Proceedings of the 2006 Conference on Empirical Methods in Natural Language Processing (EMNLP 2006), pages 1โ8, Prague, Czech Republic. Association for Computational Linguistics.
### Attention is all you need
  * Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N Gomez, Lukasz Kaiser, and Illia Polosukhin. 2017. Attention is all you need. In Advances in Neural Information Processing Systems, pages 6000โ6010.
### BERT : Pre-training of Deep Bidirectional Transformers for Language Understanding
  * Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2018. BERT:         Pre-training of deep bidirectional transformers for language understanding. In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers), pages 4171โ4186.

### Electra : Pre-training Text Encoders as Discriminators Rather Than Generators
  * Kevin Clark, Minh-Thang Luong, Quoc V. Le, Christopher D. Manning. 2019. Electra: Pre-training text encoders as discriminators rather than generators. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers), pages 4171โ4186.

### BIDAF : Bidirectional Attention Flow for Machine Comprehension
  * Minjoon Seo, Aniruddha Kembhavi, Ali Farhadi, Hannaneh Hajishirzi. 2016. Bidirectional Attention Flow for Machine Comprehension. In Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing, pages 2129โ2139.

### Effect of Negation in Sentences on Sentiment Analysis and Polarity Detection
  * Partha Mukherjeea, Saptarshi Ghoshb, and Saptarshi Ghoshc. 2018. Effect of Negation in Sentences on Sentiment Analysis and Polarity Detection. In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, pages 2129โ2139.

### KOAS : Korean Text Offensiveness Analysis System
  * Seonghwan Kim, Seongwon Lee, and Seungwon Do. 2019. KOAS: Korean Text Offensiveness Analysis System. In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), pages 1โ11.

### Korean Unsmile Dataset
  * Seonghwan Kim, Seongwon Lee, and Seungwon Do. 2019. Korean Unsmile Dataset. In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), pages 1โ11.
# Project-status

![80%](https://geps.dev/progress/80)

# Future-work
update soon plz bare with me ๐๐ป

<hr>

# KOREAN FROM HERE / ์ฌ๊ธฐ๋ถํด ํ๊ตญ์ด ์ค๋ช์๋๋ค.
# anti-cursing

**"anti-cursing"**์ ๋ฌธ์ฅ์ด๋ ๋๊ธ์์ ๋ถ์?์?์ด๊ฑฐ๋ ๋ชจ๋? ์ข๋ฅ์ ์์ค์ ๊ฐ์งํ๊ณ? ์?ํํ๋ ํ์ด์ฌ ํจํค์ง์๋๋ค๐คฌ

๋ค๋ฅธ ํจํค์ง๋ฅผ ์ค์นํ๋ ๋ฐฉ์๊ณผ ๋์ผํ๊ฒ ํจํค์ง๋ฅผ ์ค์นํ ๋ค์ ์ฝ๋์์ ์ฌ์ฉํ? ์ ์์ต๋๋ค.

Pypi(https://pypi.org/project/anti-cursing/0.0.2/)์ ํจํค์ง๋ฅด ์๋ก๋ํ์ต๋๋ค. ์ด๊ณณ์์ ํ์ธํ์ค ์ ์์ต๋๋ค.

**๐๐ปํจํค์ง๋ฅผ ์ฒ์ ์ค์นํ์๊ณ? ์ฌ์ฉํ์ค ๋ ๋ฅ๋ฌ๋ ๋ชจ๋ธ์ ๋ถ๋ฌ์ค๊ธฐ ์ํด huggingface์์ parsing์ ์๋ํฉ๋๋ค. ์ฒ์์๋ง ํด๋น ์์์ด ํ์ํ๋ ์๊ฐ์ด ์กฐ๊ธ ๊ฑธ๋ฆผ๊ณผ ์ฉ๋์ ์ฐจ์งํจ์ ๊ณ?๋?คํด์ฃผ์ธ์**

<img width="1134" alt="image" src="https://user-images.githubusercontent.com/50198431/203723736-3aeb84a1-6418-4190-b967-2888e14b14fd.png">

<hr>

# Concept

๋ฌด์ธ๊ฐ ์ฝ๋ฉ์ ํ๋ฉฐ, ๊ธ์ง ๋จ์ด๋ฅผ ๊ฐ์งํ๊ณ? ๊ทธ๊ฒ์ ๋ค๋ฅธ ๋จ์ด๋ก ๋ฐ๊ฟ์ผํ? ์ํฉ์ด ์ข์ข ์๊น๋๋ค.
๋ชจ๋? ๋ถ๋ถ์ ํ๋์ฝ๋ฉํ๋ ๊ฒ์ด ๋งค์ฐ ๋ถํธํ๋ฉฐ, ํ์ด์ฌ ์ํ๊ณ์์๋ ์ด๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํ ๋ง์ ํจํค์ง๊ฐ ์์ต๋๋ค.
๊ทธ ์ค ํ๋๊ฐ **"anti-cursing"**์๋๋ค.

ํ๊ตญ์ด ์?์ฉ์ผ๋ก ๋์ํ๋ ํด๋น ํจํค์ง๋ ๋จ์ํ ๊ธ์ง ๋จ์ด๋ฅผ ๊ธฐ์กด์ ์ค์?ํ์ฌ ๋ฐ๊พธ๋ ๊ฒ์ด ์๋, ๋ฅ๋ฌ๋ ๋ชจ๋ธ์ ํ์ตํ์ฌ ๊ธ์ง ๋จ์ด๋ฅผ ๊ฐ์งํ๊ณ? ๋ฐ๊ฟ๋๋ค.
๋ฐ๋ผ์ ์๋กญ๊ฒ ์๊ธฐ๋ ์์ฑ ๋จ์ด์ ๋ํด์๋ ํ์ต๋ง ์ด๋ฃจ์ด์ง๋ค๋ฉด ์ฝ๊ฒ ๋์ฒํ? ์ ์์ต๋๋ค.
์ด๋ฅผ ์ํด pseudo labeling์ ํตํ semi-supervied learning์ ์ฌ์ฉํฉ๋๋ค. 

์ถ๊ฐ๋ก ์์ฑ๋จ์ด๋ฅผ ---๋ ***๊ฐ์ ํน์๋ฌธ์๋ก ๋ณ๊ฒฝํ๋ ๊ฒ์ด ์๋, ์ด๋ชจ์ง๋ก ๋ณํํ์ฌ ๋์ฑ ์์ฐ์ค๋ฝ๊ฒ ๋ฐ๊ฟ ์ ์์ต๋๋ค.
# ๋ชฉ์ฐจ

- [์ค์น](#์ค์น)
- [์ฌ์ฉ๋ฒ](#์ฌ์ฉ๋ฒ)
- [๋ชจ๋ธ ์ฑ๋ฅ ๋น๊ต](#๋ชจ๋ธ-์ฑ๋ฅ-๋น๊ต)
- [๋ฐ์ดํฐ์](#๋ฐ์ดํฐ์)
- [์ฌ์ฉ API](#์ฌ์ฉ-api)
- [License](#license)
- [์ฐธ๊ณ?๋ฌธํ](#์ฐธ๊ณ?๋ฌธํ)
- [์งํ์ํฉ](#์งํ์ํฉ)
- [๋ฐ์?](#๋ฐ์?)


# ์ค์น

pip๋ฅผ ์ฌ์ฉํ์ฌ ํจํค์ง๋ฅผ ์ค์นํ? ์ ์์ต๋๋ค.
```bash
pip install anti-cursing
```

https://user-images.githubusercontent.com/50198431/204080250-4096d3d2-c51d-4d22-9756-312c6fd0aedc.mp4

# ์ฌ์ฉ๋ฒ

```python
from anti_cursing.utils import antiCursing

antiCursing.anti_cur("๋๋ ๋๊ฐ ์ข์ง๋ง, ๋๋ ๋๋ฌด ๊ฐ์๋ผ์ผ")
```

```bash
๋๋ ๋๊ฐ ์ข์ง๋ง, ๋๋ ๋๋ฌด ๐ผ๐ป์ผ
```

https://user-images.githubusercontent.com/50198431/204080262-c50bd5a2-345b-4265-a952-812abb3d9702.mp4


# ๋ชจ๋ธ ์ฑ๋ฅ ๋น๊ต
| Classification | KcElectra | KoBERT | RoBERTa-base | RoBERTa-large |
| --- | --- | --- | --- | --- |
| Validation Accuracy | 0.88680 | 0.85721 | 0.83421 | 0.86994 |
| Validation Loss | 1.00431 | 1.23237 | 1.30012 | 1.16179 |
| Training Loss | 0.09908 | 0.03761 | 0.0039 | 0.06255 |
| Epoch | 10 | 40 | 20 | 20 |
| Batch-size | 8 | 32 | 16 | 32 |
| transformers | beomi/KcELECTRA-base | skt/kobert-base-v1 | xlm-roberta-base | klue/roberta-large |


# ๋ฐ์ดํฐ์
* ### Smilegate-AI 
  * https://github.com/smilegate-ai/korean_unsmile_dataset
  * ํ๊ตญ์ด ๊ฐ์?๋ถ๋ฅ ๋ฐ์ดํฐ์
  * [paper](#korean-unsmile-dataset)
* ### ๋ค์ด๋ฒ ๋ด์ค ๊ธฐ์ฌ ํฌ๋กค๋ง
  * https://news.naver.com
  * ํ์คํธ๋ฅผ ์ํ ๋ฐ์ดํฐ์
* ### ๐ ์ด๋ชจ์ง ์?๋์ฝ๋ ๋ฐ์ดํฐ์
  * https://unicode.org/emoji/charts/full-emoji-list.html

# ์ฌ์ฉ API
### Google translator
* https://cloud.google.com/translate/docs (API ๋ฌธ์)

# License

์ด ํ๋ก์?ํธ๋ MIT ๋ผ์ด์ผ์ค๋ฅผ ๋ฐ๋ฆ๋๋ค. ์์ธํ ๋ด์ฉ์ LICENSE ํ์ผ์ ์ฐธ๊ณ?ํด์ฃผ์ธ์.

๋ผ์ด์ผ์ค ์?๋ณด --> [License](LICENSE)

# ์ฐธ๊ณ?๋ฌธํ

### Sentiment Analysis Based on Deep Learning : A Comparative Study
  * Nhan Cach Dang, Maria N. Moreno-Garcia, Fernando De la Prieta. 2006. Sentiment Analysis Based on Deep Learning : A Comparative Study. In Proceedings of the 2006 Conference on Empirical Methods in Natural Language Processing (EMNLP 2006), pages 1โ8, Prague, Czech Republic. Association for Computational Linguistics.
### Attention is all you need
  * Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N Gomez, Lukasz Kaiser, and Illia Polosukhin. 2017. Attention is all you need. In Advances in Neural Information Processing Systems, pages 6000โ6010.
### BERT : Pre-training of Deep Bidirectional Transformers for Language Understanding
  * Jacob Devlin, Ming-Wei Chang, Kenton Lee, and Kristina Toutanova. 2018. BERT:         Pre-training of deep bidirectional transformers for language understanding. In Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers), pages 4171โ4186.

### Electra : Pre-training Text Encoders as Discriminators Rather Than Generators
  * Kevin Clark, Minh-Thang Luong, Quoc V. Le, Christopher D. Manning. 2019. Electra: Pre-training text encoders as discriminators rather than generators. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers), pages 4171โ4186.

### BIDAF : Bidirectional Attention Flow for Machine Comprehension
  * Minjoon Seo, Aniruddha Kembhavi, Ali Farhadi, Hannaneh Hajishirzi. 2016. Bidirectional Attention Flow for Machine Comprehension. In Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing, pages 2129โ2139.

### Effect of Negation in Sentences on Sentiment Analysis and Polarity Detection
  * Partha Mukherjeea, Saptarshi Ghoshb, and Saptarshi Ghoshc. 2018. Effect of Negation in Sentences on Sentiment Analysis and Polarity Detection. In Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing, pages 2129โ2139.

### KOAS : Korean Text Offensiveness Analysis System
  * Seonghwan Kim, Seongwon Lee, and Seungwon Do. 2019. KOAS: Korean Text Offensiveness Analysis System. In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), pages 1โ11.

### Korean Unsmile Dataset
  * Seonghwan Kim, Seongwon Lee, and Seungwon Do. 2019. Korean Unsmile Dataset. In Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP), pages 1โ11.
# ์งํ์ํฉ

![80%](https://geps.dev/progress/80)

# ๋ฐ์?
์์ผ๋ก ์ถ๊ฐ๋? ์์?์๋๋ค ์?์๋ง ๊ธฐ๋ค๋?ค์ฃผ์ธ์๐๐ป

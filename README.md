# Quin
An easy to use framework for large-scale fact-checking and question answering.

[<a href="https://quin.algoprog.com">Demo</a>] - [<a href="https://www.researchgate.net/publication/342815574_Latent_Retrieval_for_Large-Scale_Fact-Checking_and_Question_Answering_with_NLI_training">Paper</a>] - [<a href="https://towardsdatascience.com/building-a-semantic-search-engine-for-large-scale-fact-checking-and-question-answering-9aa356632432">Blog post</a>] - [<a href="https://docs.google.com/presentation/d/1QpDF4xWgLSF-2DC1q5M_9MN7pASn-2T6NgKkhJ-NTZ8/edit?usp=sharing">Presentation</a>] - [<a href="https://archive.org/details/factual-nli">Factual-NLI Dataset</a>]

<img src="https://miro.medium.com/max/1400/1*-LaR_PfEbfJcH_BpD0Sptg.png" width="500"/>

## Usage

1) Download the model weights (encoder, passage ranker, NLI) from <a href="https://drive.google.com/file/d/1dBMCxa7xYvGNMZGyonOQO1nyoB_CgXAe/view?usp=sharing">here</a> and extract them into the models/weights folder.

2) Install the required packages:
```
pip3 install -r requirements.txt
```

3) Index a list of documents:
```python3
q = Quin(mode='index', index_path='index')
q.index_documents(documents=[
    'Document text 1',
    'Document text 2'
])
```

5) Serve a Flask API:
```python3
q = Quin(mode='serve', index_path='index')
q.serve()
```

## To do

- [ ] Include a basic frontend
- [ ] Release of the "Question - Short Answer" to "Well formed answer" T5 model
- [ ] Multilingual QR-BERT, Passage Ranker and NLI models
- [ ] Factual-NLI 2.0 with more diverse synthetic examples

## Citation

```
@techreport{samarinas2020latent,
  title={Latent Retrieval for Large-Scale Fact-Checking and Question Answering with NLI training},
  author={Samarinas, Chris and Hsu, Wynne and Lee, Mong Li},
  year={2020},
  institution={EasyChair}
}
```

<br>

<<<<<<< HEAD
# System Architectures


## Modelling Development Phase

### Data

```mermaid
stateDiagram-v2
  id1:  image<br>container<br>DatasetDict<br>builder
  [*] --> id1: from S3 bucket<br>of raw data
  id1 --> [*]: to S3 bucket of<br>DatasetDict sets
```

<br>
<br>

### Training & Validation Stage

Each container focuses on the development of a single abstractive text summarisation model.  In each case the container outputs, and saves, a model and evaluation results.

* T5: [Text to Text Transfer Transformer](https://arxiv.org/abs/1910.10683)
* PEGASUS:
    * [PEGASUS: Pre-training with Extracted Gap-sentences for Abstractive Summarization](https://arxiv.org/abs/1912.08777)
    * [PEGASUS: A State-of-the-Art Model for Abstractive Text Summarization](https://research.google/blog/pegasus-a-state-of-the-art-model-for-abstractive-text-summarization/)
* [BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension](https://arxiv.org/abs/1910.13461)

```mermaid
stateDiagram-v2
  
  id1: T5<br>image<br>container
  id2: PEGASUS<br>image<br>container
  id3: BART<br>image<br>container
  id4: Failure<br>Notification
  id5: Failure<br>Notification
  id6: Failure<br>Notification

  [*] --> T5
  [*] --> PEGASUS: DatasetDict from<br>S3 bucket
  [*] --> BART
  
  state T5 {
    [*] --> id1
    id1 --> id4: catch
    id1 --> [*]
    id4 --> [*]
  }
  state PEGASUS {
    [*] --> id2
    id2 --> id5: catch
    id2 --> [*]
    id5 --> [*]
  }
  state BART {
    [*] --> id3
    id3 --> id6: catch
    id3 --> [*]
    id6 --> [*]
  }
```

<br>
<br>

### Parallel Testing

<img src="../../../assets/arc-testing.png" alt="Testing">

=======
# System Architecture
>>>>>>> 735de18316d6f1077f32c46baa40014d41170c6f

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>
<div itemscope itemtype="http://schema.org/Dataset">
  <div itemscope itemprop="includedInDataCatalog" itemtype="http://schema.org/DataCatalog">
    <meta itemprop="name" content="TensorFlow Datasets" />
  </div>
  <meta itemprop="name" content="wmt18_translate" />
  <meta itemprop="description" content="Translate dataset based on the data from statmt.org.&#10;&#10;Versions exists for the different years using a combination of multiple data&#10;sources. The base `wmt_translate` allows you to create your own config to choose&#10;your own data/language pair by creating a custom `tfds.translate.wmt.WmtConfig`.&#10;&#10;```&#10;config = tfds.translate.wmt.WmtConfig(&#10;    version=&quot;0.0.1&quot;,&#10;    language_pair=(&quot;fr&quot;, &quot;de&quot;),&#10;    subsets={&#10;        tfds.Split.TRAIN: [&quot;commoncrawl_frde&quot;],&#10;        tfds.Split.VALIDATION: [&quot;euelections_dev2019&quot;],&#10;    },&#10;)&#10;builder = tfds.builder(&quot;wmt_translate&quot;, config=config)&#10;```&#10;&#10;To use this dataset:&#10;&#10;```python&#10;import tensorflow_datasets as tfds&#10;&#10;ds = tfds.load(&#x27;wmt18_translate&#x27;, split=&#x27;train&#x27;)&#10;for ex in ds.take(4):&#10;  print(ex)&#10;```&#10;&#10;See [the guide](https://www.tensorflow.org/datasets/overview) for more&#10;informations on [tensorflow_datasets](https://www.tensorflow.org/datasets).&#10;&#10;" />
  <meta itemprop="url" content="https://www.tensorflow.org/datasets/catalog/wmt18_translate" />
  <meta itemprop="sameAs" content="http://www.statmt.org/wmt18/translation-task.html" />
  <meta itemprop="citation" content="@InProceedings{bojar-EtAl:2018:WMT1,&#10;  author    = {Bojar, Ond{r}ej  and  Federmann, Christian  and  Fishel, Mark&#10;    and Graham, Yvette  and  Haddow, Barry  and  Huck, Matthias  and&#10;    Koehn, Philipp  and  Monz, Christof},&#10;  title     = {Findings of the 2018 Conference on Machine Translation (WMT18)},&#10;  booktitle = {Proceedings of the Third Conference on Machine Translation,&#10;    Volume 2: Shared Task Papers},&#10;  month     = {October},&#10;  year      = {2018},&#10;  address   = {Belgium, Brussels},&#10;  publisher = {Association for Computational Linguistics},&#10;  pages     = {272--307},&#10;  url       = {http://www.aclweb.org/anthology/W18-6401}&#10;}" />
</div>

# `wmt18_translate`


Warning: Manual download required. See instructions below.

*   **Description**:

Translate dataset based on the data from statmt.org.

Versions exists for the different years using a combination of multiple data
sources. The base `wmt_translate` allows you to create your own config to choose
your own data/language pair by creating a custom `tfds.translate.wmt.WmtConfig`.

```
config = tfds.translate.wmt.WmtConfig(
    version="0.0.1",
    language_pair=("fr", "de"),
    subsets={
        tfds.Split.TRAIN: ["commoncrawl_frde"],
        tfds.Split.VALIDATION: ["euelections_dev2019"],
    },
)
builder = tfds.builder("wmt_translate", config=config)
```

*   **Homepage**:
    [http://www.statmt.org/wmt18/translation-task.html](http://www.statmt.org/wmt18/translation-task.html)

*   **Source code**:
    [`tfds.translate.Wmt18Translate`](https://github.com/tensorflow/datasets/tree/master/tensorflow_datasets/translate/wmt18.py)

*   **Versions**:

    *   **`1.0.0`** (default): No release notes.

*   **Manual download instructions**: This dataset requires you to
    download the source data manually into `download_config.manual_dir`
    (defaults to `~/tensorflow_datasets/downloads/manual/`):<br/>
    Some of the wmt configs here, require a manual download.
    Please look into wmt.py to see the exact path (and file name) that has to
    be downloaded.

*   **Figure**
    ([tfds.show_examples](https://www.tensorflow.org/datasets/api_docs/python/tfds/visualization/show_examples)):
    Not supported.

*   **Citation**:

```
@InProceedings{bojar-EtAl:2018:WMT1,
  author    = {Bojar, Ond{r}ej  and  Federmann, Christian  and  Fishel, Mark
    and Graham, Yvette  and  Haddow, Barry  and  Huck, Matthias  and
    Koehn, Philipp  and  Monz, Christof},
  title     = {Findings of the 2018 Conference on Machine Translation (WMT18)},
  booktitle = {Proceedings of the Third Conference on Machine Translation,
    Volume 2: Shared Task Papers},
  month     = {October},
  year      = {2018},
  address   = {Belgium, Brussels},
  publisher = {Association for Computational Linguistics},
  pages     = {272--307},
  url       = {http://www.aclweb.org/anthology/W18-6401}
}
```


## wmt18_translate/cs-en (default config)

*   **Config description**: WMT 2018 cs-en translation task dataset.

*   **Download size**: `1.89 GiB`

*   **Dataset size**: `3.84 GiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    No

*   **Splits**:

Split          | Examples
:------------- | ---------:
`'test'`       | 2,983
`'train'`      | 24,021,877
`'validation'` | 3,005

*   **Feature structure**:

```python
Translation({
    'cs': Text(shape=(), dtype=tf.string),
    'en': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
cs      | Text        |       | tf.string |
en      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('cs', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script>
const url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/wmt18_translate-cs-en-1.0.0.html";
const dataButton = document.getElementById('displaydataframe');
dataButton.addEventListener('click', async () => {
  // Disable the button after clicking (dataframe loaded only once).
  dataButton.disabled = true;

  const contentPane = document.getElementById('dataframecontent');
  try {
    const response = await fetch(url);
    // Error response codes don't throw an error, so force an error to show
    // the error message.
    if (!response.ok) throw Error(response.statusText);

    const data = await response.text();
    contentPane.innerHTML = data;
  } catch (e) {
    contentPane.innerHTML =
        'Error loading examples. If the error persist, please open '
        + 'a new issue.';
  }
});
</script>

{% endframebox %}

<!-- mdformat on -->

## wmt18_translate/de-en

*   **Config description**: WMT 2018 de-en translation task dataset.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
Translation({
    'de': Text(shape=(), dtype=tf.string),
    'en': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
de      | Text        |       | tf.string |
en      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('de', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

## wmt18_translate/et-en

*   **Config description**: WMT 2018 et-en translation task dataset.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
Translation({
    'en': Text(shape=(), dtype=tf.string),
    'et': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
en      | Text        |       | tf.string |
et      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('et', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

## wmt18_translate/fi-en

*   **Config description**: WMT 2018 fi-en translation task dataset.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
Translation({
    'en': Text(shape=(), dtype=tf.string),
    'fi': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
en      | Text        |       | tf.string |
fi      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('fi', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

## wmt18_translate/kk-en

*   **Config description**: WMT 2018 kk-en translation task dataset.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
Translation({
    'en': Text(shape=(), dtype=tf.string),
    'kk': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
en      | Text        |       | tf.string |
kk      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('kk', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

## wmt18_translate/ru-en

*   **Config description**: WMT 2018 ru-en translation task dataset.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
Translation({
    'en': Text(shape=(), dtype=tf.string),
    'ru': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
en      | Text        |       | tf.string |
ru      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('ru', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

## wmt18_translate/tr-en

*   **Config description**: WMT 2018 tr-en translation task dataset.

*   **Download size**: `59.32 MiB`

*   **Dataset size**: `63.78 MiB`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Yes

*   **Splits**:

Split          | Examples
:------------- | -------:
`'test'`       | 3,000
`'train'`      | 205,756
`'validation'` | 3,007

*   **Feature structure**:

```python
Translation({
    'en': Text(shape=(), dtype=tf.string),
    'tr': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
en      | Text        |       | tf.string |
tr      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('tr', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):

<!-- mdformat off(HTML should not be auto-formatted) -->

{% framebox %}

<button id="displaydataframe">Display examples...</button>
<div id="dataframecontent" style="overflow-x:auto"></div>
<script>
const url = "https://storage.googleapis.com/tfds-data/visualization/dataframe/wmt18_translate-tr-en-1.0.0.html";
const dataButton = document.getElementById('displaydataframe');
dataButton.addEventListener('click', async () => {
  // Disable the button after clicking (dataframe loaded only once).
  dataButton.disabled = true;

  const contentPane = document.getElementById('dataframecontent');
  try {
    const response = await fetch(url);
    // Error response codes don't throw an error, so force an error to show
    // the error message.
    if (!response.ok) throw Error(response.statusText);

    const data = await response.text();
    contentPane.innerHTML = data;
  } catch (e) {
    contentPane.innerHTML =
        'Error loading examples. If the error persist, please open '
        + 'a new issue.';
  }
});
</script>

{% endframebox %}

<!-- mdformat on -->

## wmt18_translate/zh-en

*   **Config description**: WMT 2018 zh-en translation task dataset.

*   **Download size**: `Unknown size`

*   **Dataset size**: `Unknown size`

*   **Auto-cached**
    ([documentation](https://www.tensorflow.org/datasets/performances#auto-caching)):
    Unknown

*   **Splits**:

Split | Examples
:---- | -------:

*   **Feature structure**:

```python
Translation({
    'en': Text(shape=(), dtype=tf.string),
    'zh': Text(shape=(), dtype=tf.string),
})
```

*   **Feature documentation**:

Feature | Class       | Shape | Dtype     | Description
:------ | :---------- | :---- | :-------- | :----------
        | Translation |       |           |
en      | Text        |       | tf.string |
zh      | Text        |       | tf.string |

*   **Supervised keys** (See
    [`as_supervised` doc](https://www.tensorflow.org/datasets/api_docs/python/tfds/load#args)):
    `('zh', 'en')`

*   **Examples**
    ([tfds.as_dataframe](https://www.tensorflow.org/datasets/api_docs/python/tfds/as_dataframe)):
    Missing.

# Attention-Based Neural Networks — Image Captioning

Demo notebooks for image captioning with and without attention mechanisms, using the Flickr8k dataset.

## Notebooks

| Notebook | Description |
|---|---|
| `demo_01_ImageCaptioningWithoutAttention.ipynb` | Baseline image captioning model without attention |
| `demo_02_ImageCaptioningUsingAttention.ipynb` | Image captioning using an attention mechanism |

---

## Dataset Files

The large dataset files have been split into 45 MB parts for GitHub compatibility.
Follow the steps below to reassemble them before running the notebooks.

### 1. Reconstruct `datasets/flickr8k.zip`

```bash
cat datasets/parts/flickr8k.zip.part_* > datasets/flickr8k.zip
unzip datasets/flickr8k.zip -d datasets/
rm datasets/flickr8k.zip
```

### 2. Reconstruct and extract `flickr8k/images/`

```bash
cat flickr8k/image_parts/images.zip.part_* > flickr8k/images.zip
unzip flickr8k/images.zip -d .
rm flickr8k/images.zip
```

### 3. Verify

```bash
# Should print ~8000
ls flickr8k/images/ | wc -l
```

---

## Requirements

Python 3.8+, TensorFlow 2.x, and any packages listed in the notebooks.

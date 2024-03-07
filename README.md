### Setup

To generate the static files for the website in `output`, run the [pelican](https://getpelican.com) command:

```
conda create -n website python=3.10 -y
conda activate website
pip install -r requirements.txt
pelican --autoreload --listen
```
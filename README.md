### Setup

To generate the static files for the website in `output`, run the [pelican](https://getpelican.com) command:

```
conda create -n website python=3.10 -y
conda activate website
pip install -r requirements.txt
pelican --autoreload --listen
cp -a output docs
```

Then go to the github repo Settings -> Pages, set the branch as `main` and folder as `docs`.
Click `save` and the website should be deployed automatically.
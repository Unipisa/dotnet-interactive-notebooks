# .NET interactive-notebooks

Forked from [colombod/interactive-notebooks](https://github.com/colombod/interactive-notebooks) after [@colombod webinar](https://youtu.be/g67_d5pY_Uk) ([slides](https://www.fondazionecrui.it/wp-content/uploads/2020/10/NET-Interactive-piattaforma-opensource-per-insegnare-computer-science-e-data-science.pdf))

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Unipisa/dotnet-interactive-notebooks/main?urlpath=lab/master)

This repo contains notebooks that use [.NET Interactive](https://github.com/dotnet/interactive) kernel

## Install on existing JupyterHub installation

We can build the docker from the repo using [repo2docker](https://github.com/jupyterhub/repo2docker)

```
pip install jupyter-repo2docker
jupyter-repo2docker https://github.com/Unipisa/dotnet-interactive-notebooks
```

We can see the name of the built image by

```
sudo docker image ls
```

and we can add to existing JupiterHub installation by editing `jupyter_config.py` on the `c.DockerSpawner.image_whitelist` as 

```
c.DockerSpawner.image_whitelist = {
        'DEV - .NET interactive' : '$NAME_OF_DOCKER_BILT_IMAGE'
        }       
```

## Use on Unipi installation

Unipi users can try on [jupyterhub.polo2.sid.unipi.it](https://jupyterhub.polo2.sid.unipi.it:8000/) or [jupyterhubfm.df.unipi.it](https://jupyterhubfm.df.unipi.it:8000/) accessing via their credentials.


# Generative Ozzy Art

## Introduction

The `generative-ozzy-art` repository is a library for creating generative art, based upon the original repository for [Scrappy Squirrels](https://www.scrappysquirrels.co/). It was originally developed by [Rounak Banik](https://github.com/rounakbanik) for the purpose of creating NFT avatar & collectible projects.

## Features

### Generate over a million distinct images with less than 60 traits

The library allows you to generate images every distinct possible combination of your traits. For context, if you had trait art for a project like [Bored Apes](https://boredapeyachtclub.com/#/home), the library could generate upwards of 1.2 billion distinct apes.

### Add rarity weights

The library also allows you to configure the image generation process in such a way that you have complete control over how rare each and every trait is.

### Generate compliant JSON metadata for your NFTs

There is now an added functionality to generate JSON metadata for your NFTs that are in compliance with OpenSea metadata requirements (and by extension, the general NFT metadata standard).

### Fuzzy friendly

This library can be used even if you do not know how to program (in `Python` or otherwise). THe original repository author put out a [Tutorial](https://medium.com/scrappy-squirrels/tutorial-create-generative-nft-art-with-rarities-8ee6ce843133) for more details on how to use (non-technical) and extend (technical) the library.

## Installation

These instructions assume you already have at least [Python 3](https://www.python.org/downloads/) and [Git](https://git-scm.com/downloads) installed for your respective system.

### Clone this repository

```shell
git clone https://github.com/osmo-support-lab/generative-ozzy-art.git
```

### Create the Virtual Environment

Make sure you are in the main directory for the repository.

```shell
cd <path>/<to>/generative-ozzy-art
```

The following command creates a virtual environment where all packages and python requirements can exist without needing to be installed globally. **NOTE:** On some operating systems you might need to replace `python` with `python3`.

```shell
python -m venv venv
```

### Activate the Venv (Virtual Environment)

In order to properly utilize the environment, you must "Activate" it. This means that your shell will direct all commands to take place *within* the `venv` file.

Linux/MacOS:

```shell
source venv/bin/activate
```

On Windows (cmd.exe):

```shell
venv\Scripts\activate.bat
```

On Windows (Powershell):

```ps
venv\Scripts\Activate.ps1
```

### Install the required packages

```shell
pip install Pillow pandas progressbar2
```

### Add Assets/Information

Place your assets in logically named folders within `assets`, and ensure you update [`config.py`](config.py) to match.

### Make those NFTs

Run `python nft.py` in the repository folder.

### Make Metadata

In order to generate JSON metadata, define `BASE_NAME`, `BASE_IMAGE_URL`, and `BASE_JSON` in [`metadata.py`](metadata.py).

Then run `python metadata.py`.

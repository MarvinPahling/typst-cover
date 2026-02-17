# My Personal Cover for University Stuff

## Installation

```bash
git clone https://github.com/MarvinPahling/typst-cover.git $XDG_DATA_HOME/typst/packages/marvin/cover
```

Update with

```bash
git -C $XDG_DATA_HOME/typst/packages/marvin/cover pull
```

## Usage

You can eather invoce the cover directly like this

```typst
#import "@marvin/cover:1.0.0": cover

#cover(
    title: "",
    subtitle: "",
    course: "",
    authors: ((name: "", id: ""),),
    author-label: "Author: ",
    id-label: "ID: ",
    date-label: "Data: ",
    institution: "",
    department: "",
    logo: "mtu" | "ostfalia" | "path/to/logo.svg",
    display-logo: true,
  )
```

Or load the text contents from a yaml file with the following schema

```yaml
title: "Assingment 1"
subtitle: "Some technical stuff"
course: "AI NFT Buzzwording 101"
authors:
  -marvin:
    name: "Marvin"
    id: "1234"
date-label: "Date:"
author-labels:
  name: "Author"
  id: "ID"
institution: "MIT"
department: "Computer Science"
logo:
  path: "./logos/ostfalia.svg"
  display: true
```

```typst
#import "@marvin/cover:1.0.0": load_from_yaml

#load_from_yaml(path: "./example-config")
```

## Refs

- (https://marketing.mtu.ie/logos)[MTU Logo]
- (https://de.wikipedia.org/wiki/Datei:Ostfalia.svg)[Ostfalia Logo]

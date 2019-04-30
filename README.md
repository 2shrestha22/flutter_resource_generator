# flutter_asset_generator

Automatically generate the dart file for pubspec.yaml

The purpose of this library is to help flutter developers automatically generate asset corresponding dart files to help developers release their hands from this meaningless job, and the open source community has a lot of the same functionality.

This library is based on dartlang's build library.

[中文文档](https://github.com/CaiJingLong/flutter_resource_generator/blob/master/README_CHN.md)

[English](https://github.com/CaiJingLong/flutter_resource_generator)

- [flutter_asset_generator](#flutterassetgenerator)
  - [screenshot](#screenshot)
  - [Usage](#usage)
    - [use source](#use-source)
    - [pub global](#pub-global)
  - [File name](#file-name)

## screenshot

![img](https://raw.githubusercontent.com/CaiJingLong/some_asset/master/asset_gen_3.0.gif)

## Usage

### use source

add `dart`,`pub` to `$PATH` environment.

```bash
git clone https://github.com/CaiJingLong/flutter_resource_generator.git
cd flutter_resource_generator
pub get
dart bin/resource_generator.dart $flutter_project
```

### pub global

install:

```bash
pub global activate flutter_asset_generator
```

use:

`fgen $flutter_project`

## File name

convert filed name example:

    images/1.png => IMAGES_PNG
    images/hello_world.jpg => IMAGES_HELLO_WORLD_JPG

Errors will occur in the following situations

```bash
  images/
    main_login.png
    main/
      login.png
```

Because the two field names will be exactly the same.

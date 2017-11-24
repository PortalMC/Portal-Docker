# Portal-Docker

## Usage

Build Docker image.

```
./gradlew build -Pversion={imagename}-{version}

# example
./gradlew build -Pversion=builder-1.12.2-1
```

Push image.

```
./gradlew push -Pversion={imagename}-{version}

# example
./gradlew push -Pversion=builder-1.12.2-1
```

## License

Copyright 2017 Tamaki Hidetsugu (Ralph) and other contributors

This program is licensed under [GNU Affero General Public License, version 3](LICENSE)
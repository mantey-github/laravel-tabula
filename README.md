# laravel-tabula
laravel-tabula is a tool for liberating data tables trapped inside PDF files for the Laravel framework. This package was inspired by Python’s tabula-py package.

### How to install


```
composer require initred/laravel-tabula
```

### Configuration Settings (Needed Java)

[Windows]

http://www.oracle.com/technetwork/java/javase/downloads/index.html.
Please System Path Adding.

[Mac os]

```
brew update
```
```
brew cask install java
```

[Debian]

```
sudo apt install default-jre
```

[Fedora]

```
sudo dnf install java-latest-openjdk
```

### How to use on Laravel (Example)

```
$tabula = new Tabula('/usr/bin/');

$tabula->convertInto(
  storage_path('app/public/pdf/test.pdf'),
  storage_path('app/public/json/test.csv'),
  'csv',
  'all'
);

$tabula->convertIntoByBatch(
  storage_path('app/public/pdf'),
  'json',
  'all'
);
```

### License

laravel-tabula is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

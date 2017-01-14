# angel_framework

[![pub 1.0.0-dev.44](https://img.shields.io/badge/pub-1.0.0--dev.44-red.svg)](https://pub.dartlang.org/packages/angel_framework)
[![build status](https://travis-ci.org/angel-dart/framework.svg)](https://travis-ci.org/angel-dart/framework)

Core libraries for the Angel Framework.

```dart
import 'package:angel_framework/angel_framework.dart';

main() async {
  var app = new Angel();

  app
    ..get('/hello', (req, res) {
      res.write('world!');
    })
    ..post('/date', () => new DateTime.now().toString());

  await app.startServer();
}
```
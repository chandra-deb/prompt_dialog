# Prompt Dialog

[![pub package](https://img.shields.io/pub/v/prompt_dialog.svg)](https://pub.dartlang.org/packages/prompt_dialog)

Prompt Dialog Widget for Flutter(JS-LIKE).
https://pub.dev/packages/prompt_dialog

## Installation

### Add pubspec.yaml
``` yaml
dependencies:
  prompt_dialog: lastest_version
```
---
## Example

### Basic
``` dart
import 'package:flutter/material.dart';

import 'package:prompt_dialog/prompt_dialog.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Center(
          child: FlatButton(
            child: Text('Prompt Dialog'),
            onPressed: () async {
              return print(await prompt(context));
            },
          ),
        ),
      ),
    );
  }
}
```

### Custom Message
``` dart
import 'package:flutter/material.dart';

import 'package:prompt_dialog/prompt_dialog.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Center(
          child: FlatButton(
            child: Text('Prompt Dialog'),
            onPressed: () async {
              return print(await prompt(
                context,
                title: Text('Would you like to remove?'),
                initialValue: 'Sure',
                textOK: Text('Yes'),
                textCancel: Text('No'),
                autoFocus: true,
              ));
            },
          ),
        ),
      ),
    );
  }
}
```
---
## Recommend Libraries

- [Confirm Dialog](https://github.com/gtgalone/confirm_dialog) - Confirm Dialog Widget for Flutter(JS-LIKE).
- [Alert Dialog](https://github.com/gtgalone/alert_dialog) - Alert Dialog Widget for Flutter(JS-LIKE).

## Maintainer

- [Jehun Seem](https://github.com/gtgalone)

## License

MIT

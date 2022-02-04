# Avatar stack package for Flutter

[![Build Status](https://github.com/cyrax111/avatar_stack/workflows/Dart%20CI/badge.svg)](https://github.com/cyrax111/avatar_stack/actions?query=workflow%3A"Dart+CI"+branch%3Amaster)
[![Coverage Status](https://coveralls.io/repos/github/cyrax111/avatar_stack/badge.svg?branch=master)](https://coveralls.io/github/cyrax111/avatar_stack?branch=master)
[![Pub](https://img.shields.io/pub/v/avatar_stack)](https://pub.dev/packages/avatar_stack)

Avatar stack is used to visually represent users, places, and things in an app.

![Example](https://github.com/cyrax111/blob/raw/master/avatar_stack/feature1.gif?raw=true)


## Features


### Restrict amount of items
Usually the stack avatar shows all items as possible but you can restrict it by, say, five items.
![Restrict amount of items](https://github.com/cyrax111/blob/raw/master/avatar_stack/restricted_amount.gif?raw=true)


### Alignment
By default the stack avatar has left alignment one can change it.
#### *center alignment*
![center alignment](https://github.com/cyrax111/blob/raw/master/avatar_stack/center_alignment.gif?raw=true)
#### *right alignment*
![right alignment](https://github.com/cyrax111/blob/raw/master/avatar_stack/right_alignment.gif?raw=true)


### Coverage
You can set how avatars will coverage each others. 
#### *max coverage is set to 70%*
![max coverage is set to 70%](https://github.com/cyrax111/blob/raw/master/avatar_stack/max_coverage.gif?raw=true)
#### *min coverage is set to minus 50%*
The negative coverage will set space between items.
![min coverage is set to minus 50%](https://github.com/cyrax111/blob/raw/master/avatar_stack/min_coverage.gif?raw=true)


### Any widget for stack
You can use any widget to stack not only avatars
![Any widget for stack](https://github.com/cyrax111/blob/raw/master/avatar_stack/stack_widgets.gif?raw=true)

### Indent of an info item
The additional space between an info item (if exists) and other items.
![Indent of an info item](https://github.com/cyrax111/blob/raw/master/avatar_stack/indent_of_the_info_widget.png?raw=true)

### Stack laying
The way to tile items.

#### *the first item is at the top*
![Indent of an info item](https://github.com/cyrax111/blob/raw/master/avatar_stack/the_first_item_is_at_the_top.png?raw=true)

#### *the fifth item is at the top*
![Indent of an info item](https://github.com/cyrax111/blob/raw/master/avatar_stack/the_fifth_item_is_at_the_top.png?raw=true)

## Example

```dart
import 'package:avatar_stack/avatar_stack.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(const MaterialApp(home: AvatarStackExample()));
}

class AvatarStackExample extends StatelessWidget {
  const AvatarStackExample({Key? key}) : super(key: key);
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(),
      body: Center(
        child: Padding(
          padding: const EdgeInsets.all(8.0),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              const Text(
                'Example:',
              ),
              const SizedBox(height: 20),
              AvatarStack(
                height: 50,
                avatars: [
                  for (var n = 0; n < 15; n++)
                    NetworkImage('https://i.pravatar.cc/150?img=$n'),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```

You can also use the example from github [https://github.com/cyrax111/avatar_stack/tree/master/example](https://github.com/cyrax111/avatar_stack/tree/master/example)
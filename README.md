# Toggle Switch

A simple toggle switch widget. It can be fully customized with desired icons, width, colors, text, corner radius, animation etc. It also maintains selection state.

## Getting Started

In the `pubspec.yaml` of your flutter project, add the following dependency:

```yaml
dependencies:
  ...
  toggle_switch: "^1.0.0+1"
```

Import it:

```dart
import 'package:toggle_switch/toggle_switch.dart';
```

## Usage Examples

### Basic toggle switch

```dart
// Here, default theme colors are used for activeBgColor, activeFgColor, inactiveBgColor and inactiveFgColor
ToggleSwitch(
  initialLabelIndex: 0,
  totalSwitches: 3,
  labels: ['America', 'Canada', 'Mexico'],
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![Basic toggle switch](https://media.giphy.com/media/QX1jcEQH5PnxL7l7Lh/giphy.gif)

### Basic toggle switch with custom height and font size

```dart
ToggleSwitch(
  minWidth: 90.0,
  minHeight: 90.0,
  fontSize: 16.0,
  initialLabelIndex: 1,
  activeBgColor: [Colors.green],
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.grey[900],
  totalSwitches: 3,
  labels: ['Tall', 'Grande', 'Venti'],
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![Basic toggle switch with custom height and font size](https://media.giphy.com/media/Jrf2KLuWJVaB4cIwlz/giphy.gif)

### With icons and text

```dart
ToggleSwitch(
  minWidth: 90.0,
  cornerRadius: 20.0,
  activeBgColor: [Colors.cyan],
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.white,
  totalSwitches: 2,
  labels: ['YES', 'NO'],
  icons: [FontAwesomeIcons.check, FontAwesomeIcons.times],
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![With icons and text](https://media.giphy.com/media/SwyiW7VtVf4z1UZviS/giphy.gif)

### With icons, text and different active background colors

```dart
ToggleSwitch(
  minWidth: 90.0,
  initialLabelIndex: 1,
  cornerRadius: 20.0,
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.white,
  totalSwitches: 2,
  labels: ['Male', 'Female'],
  icons: [FontAwesomeIcons.mars, FontAwesomeIcons.venus],
  activeBgColors: [[Colors.blue],[Colors.pink]],
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![With icons, text and different active background colors](https://media.giphy.com/media/ih4qpWz1wqqILVWYiT/giphy.gif)

### With border color, border width, icons, custom height and different active background colors

```dart
ToggleSwitch(
  minWidth: 90.0,
  minHeight: 70.0,
  initialLabelIndex: 2,
  cornerRadius: 20.0,
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.white,
  totalSwitches: 3,
  icons: [
    FontAwesomeIcons.mars,
    FontAwesomeIcons.venus,
    FontAwesomeIcons.transgender
  ],
  iconSize: 30.0,
  borderWidth: 2.0,
  borderColor: [Colors.blueGrey],
  activeBgColors: [[Colors.blue], [Colors.pink], [Colors.purple]],
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![With border color, border width, icons, custom height and different active background colors](https://media.giphy.com/media/yKLaQurj8KvjLaYte0/giphy.gif)

### With gradient border color, divider color and gradient active background colors

```dart
ToggleSwitch(
  minWidth: 90.0,
  minHeight: 70.0,
  initialLabelIndex: 0,
  cornerRadius: 20.0,
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.white,
  totalSwitches: 3,
  icons: [
    FontAwesomeIcons.facebook,
    FontAwesomeIcons.twitter,
    FontAwesomeIcons.instagram
  ],
  iconSize: 30.0,
  borderColor: [Color(0xff3b5998), Color(0xff8b9dc3), Color(0xff00aeff), Color(0xff0077f2), Color(0xff962fbf), Color(0xff4f5bd5)],
  dividerColor: Colors.blueGrey,
  activeBgColors: [[Color(0xff3b5998), Color(0xff8b9dc3)], [Color(0xff00aeff), Color(0xff0077f2)], [Color(0xfffeda75), Color(0xfffa7e1e), Color(0xffd62976), Color(0xff962fbf), Color(0xff4f5bd5)]],
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![With gradient border color, divider color and gradient active background colors](https://media.giphy.com/media/wIYpfehKbfQFjXmlKC/giphy.gif)

### With bounceInOut animation

```dart
ToggleSwitch(
  minWidth: 90.0,
  minHeight: 70.0,
  initialLabelIndex: 0,
  cornerRadius: 20.0,
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.white,
  totalSwitches: 2,
  icons: [
    FontAwesomeIcons.lightbulb,
    FontAwesomeIcons.solidLightbulb,
  ],
  iconSize: 30.0,
  activeBgColors: [[Colors.black45, Colors.black26], [Colors.yellow, Colors.orange]],
  animate: true, // with just animate set to true, default curve = Curves.easeIn
  curve: Curves.bounceInOut, // animate must be set to true when using custom curve
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![With bounceInOut animation](https://media.giphy.com/media/lvFBiXEnax3rznuw1V/giphy.gif)

### With radius style

```dart
ToggleSwitch(
  minWidth: 90.0,
  cornerRadius: 20.0,
  activeBgColors: [[Colors.green[800]!], [Colors.red[800]!]],
  activeFgColor: Colors.white,
  inactiveBgColor: Colors.grey,
  inactiveFgColor: Colors.white,
  initialLabelIndex: 1,
  totalSwitches: 2,
  labels: ['True', 'False'],
  radiusStyle: true,
  onToggle: (index) {
    print('switched to: $index');
  },
),
```

![With radius style](https://media.giphy.com/media/GIhOLGT1kOdz9wUQ4Y/giphy.gif)

### setState() inside onToggle

[Example code with explanation](https://github.com/PramodJoshi/toggle_switch/issues/11#issuecomment-679277018)

## Credits

[Eugene](https://stackoverflow.com/questions/56340682/flutter-equvalent-android-toggle-switch)
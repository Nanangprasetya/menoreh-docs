# Switches

Switches toggle the state of a single item on or off.

## Switches Default

=== "Design"

    ![Switch Default](/assets/images/component/action/switches.png){ loading=lazy }

=== "Implementation"

    ``` dart
    Switch(
      value: light,
      onChanged: (bool value) {}

    )
    ```

## Checkbox List Tile

=== "Design"

    ![Switch Button list tile](/assets/images/component/action/switches-tile.png){ loading=lazy }

=== "Implementation"

    ``` dart
    SwitchListTile(
      title: const Text('Switch Title'),
      value: true,
      onChanged:(bool? value) { },
    ),
    ```

## Customization

To change the whole Button Theme, please open the `core/themes/app_theme.dart`.
Here's how to change the Widget Radio Switch theme:

```dart
switchTheme: SwitchThemeData(
    fillColor: MaterialStateProperty.resolveWith<Color>((Set<MaterialState> states) {
    if (states.contains(MaterialState.selected)) {
        return AppColors.secondary;
    } else if (states.contains(MaterialState.hovered)) {
        return AppColors.splash;
    }
    return AppColors.fillPrimary;
    }),
),
```

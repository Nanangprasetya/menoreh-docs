# Radio Button

Radio buttons allow users to select one option from a set.

## Radio List Tile

=== "Design"

    ![Radio Button](/assets/images/component/action/radio_button.png){ loading=lazy }

=== "Implementation"

    ``` dart
    RadioListTile<bool>(
      onChanged:(bool? value) { },
      value: false,
      title: const Text('Radio Title'),
    ),
    ```

## Radio Button Multiple

=== "Design"

    ![Radio Button Multiple](/assets/images/component/action/radio_button-tile.png){ loading=lazy }

=== "Implementation"

    ``` dart
    Column(
        children: [
            Radio<int>(
                value: 0,
                groupValue: _groupValue,
                onChanged: (int? value) {},
            ),
            Radio<int>(
                value: 1,
                groupValue: _groupValue,
                onChanged: (int? value) {},
            ),
        ],
    )
    ```

    !!! info
        `groupValue` The currently selected value for a group of radio buttons.

## Customization

To change the whole Button Theme, please open the `core/themes/app_theme.dart`.
Here's how to change the Widget Radio Button theme:

```dart
radioTheme: RadioThemeData(
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

# Checkboxs

Checkboxes allow users to select one or more items from a set. Checkboxes can turn an option on or off.

## Checkbox Default

=== "Design"

    ![Checkbox Default](/assets/images/component/action/checkbox.png){ loading=lazy }

=== "Implementation"

    ``` dart
    Checkbox(
        value: false,
        onChanged: (bool? value) {},
    )
    ```

## Checkbox List Tile

=== "Design"

    ![Checkbox Button list tile](/assets/images/component/action/checkbox-tile.png){ loading=lazy }

=== "Implementation"

    ``` dart
    CheckboxListTile(
      onChanged:(bool? value) { },
      value: true,
      title: const Text('Checkbox Title'),
    ),
    ```

## Customization

To change the whole Button Theme, please open the `core/themes/app_theme.dart`.
Here's how to change the Widget Radio Chackboxs theme:

```dart
checkboxTheme: CheckboxThemeData(
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

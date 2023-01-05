# Common Button

Buttons allow users to take actions, and make choices, with a single tap.

Button di Menoreh Library menggunakan Tema Matrial design v2. Button terdiri dari Widget `ElevatedButton`, `OutlinedButton` dan `TextButton`.

Untuk mengubah semua Tema button silahkan pelajari berikut [ini](/documentation/component/action/common_button/#customization).

## Elevated Button

=== "Design"

    ![Elevated Button](/assets/images/component/action/button_elevated.png){ loading=lazy }

=== "Implementation"

    ```dart
    ElevatedButton(
        onPressed: (){}
        child: const Text('Text Button'),
    ),
    ```

    ??? info
        Untuk mengubah warna Button silahkan tambahkan parameter `style` didalam `ElevatedButton`

        ```dart
        style: ElevatedButton.styleFrom(
            backgroundColor: AppColors.green,
            foregroundColor: AppColors.white,
        ),
        ```

**Elevated Icon Button**
=== "Design"

    ![Elevated Button](/assets/images/component/action/button_elevated-icon.png){ loading=lazy }

=== "Implementation"

    ```dart
    ElevatedButton.icon(
        onPressed: (){}
        icon: const Icon(Icons.add),
        label: const Text('Title Button'),
      ),
    ),
    ```

    ??? info
        Untuk mengubah warna Button silahkan tambahkan parameter `style` didalam `ElevatedButton.icon`

        ```dart
        style: ElevatedButton.styleFrom(
            backgroundColor: AppColors.green,
            foregroundColor: AppColors.white,
        ),
        ```


## Outlined Button

=== "Design"

    ![Outlined Button](/assets/images/component/action/button_outlined.png){ loading=lazy }

=== "Implementation"

    ```dart
    OutlinedButton(
        onPressed: (){}
        child: const Text('Text Button'),
    ),
    ```

    ??? info
        Untuk mengubah warna Button silahkan tambahkan parameter `style` didalam `OutlinedButton`

        ```dart
        style: OutlinedButton.styleFrom(
            backgroundColor: AppColors.green,
            foregroundColor: AppColors.white,
        ),
        ```

**Outlined Icon Button**
=== "Design"

    ![Outlined Button](/assets/images/component/action/button_outlined-icon.png){ loading=lazy }

=== "Implementation"

    ```dart
    OutlinedButton.icon(
        onPressed: (){}
        icon: const Icon(Icons.add),
        label: const Text('Title Button'),
      ),
    ),
    ```

    ??? info
        Untuk mengubah warna Button silahkan tambahkan parameter `style` didalam `OutlinedButton.icon`

        ```dart
        style: OutlinedButton.styleFrom(
            backgroundColor: AppColors.green,
            foregroundColor: AppColors.white,
        ),
        ```

## Text Button

=== "Design"

    ![Text Button](/assets/images/component/action/button_text.png){ loading=lazy }

=== "Implementation"

    ```dart
    TextButton(
        onPressed: (){}
        child: const Text('Text Button'),
    ),
    ```

    ??? info
        Untuk mengubah warna Button silahkan tambahkan parameter `style` didalam `TextButton`

        ```dart
        style: TextButton.styleFrom(
            backgroundColor: AppColors.green,
            foregroundColor: AppColors.white,
        ),
        ```

**Text Icon Button**
=== "Design"

    ![Text Button](/assets/images/component/action/button_text-icon.png){ loading=lazy }

=== "Implementation"

    ```dart
    TextButton.icon(
        onPressed: (){}
        icon: const Icon(Icons.add),
        label: const Text('Title Button'),
      ),
    ),
    ```

    ??? info
        Untuk mengubah warna Button silahkan tambahkan parameter `style` didalam `TextButton.icon`

        ```dart
        style: TextButton.styleFrom(
            backgroundColor: AppColors.green,
            foregroundColor: AppColors.white,
        ),
        ```

## Customization

To change the whole Button Theme, please open the `core/themes/app_theme.dart`.
Here's how to change the Widget Buttons theme:

### Elevated Button

```dart
 elevatedButtonTheme: ElevatedButtonThemeData(
    style: ElevatedButton.styleFrom(
    shape: const StadiumBorder(),
    padding: const EdgeInsets.symmetric(horizontal: AppDimens.paddingLarge),
    foregroundColor: AppColors.white,
    backgroundColor: AppColors.primary,
    minimumSize: Size(AppDimens.size8X, AppDimens.size3XL),
    shadowColor: AppColors.transparant,
    elevation: 0,
    ),
),
```

### Outlined Button

```dart
outlinedButtonTheme: OutlinedButtonThemeData(
    style: OutlinedButton.styleFrom(
        foregroundColor: AppColors.primary,
        side: const BorderSide(width: 1.0, color: AppColors.primary),
        shape: const StadiumBorder(),
        padding: const EdgeInsets.symmetric(horizontal: AppDimens.paddingLarge),
        minimumSize: Size(AppDimens.size8X, AppDimens.size3XL),
        shadowColor: AppColors.transparant,
        elevation: 0,
    ),
),
```

### Text Button

```dart
textButtonTheme: TextButtonThemeData(
    style: TextButton.styleFrom(
        shape: const StadiumBorder(),
        padding: const EdgeInsets.symmetric(horizontal: AppDimens.paddingLarge),
        foregroundColor: AppColors.primary,
        minimumSize: Size(AppDimens.size8X, AppDimens.size3XL),
        elevation: 0,
    ),
)
```

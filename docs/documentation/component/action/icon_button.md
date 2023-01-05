# Icon Button

Icon Button allow users to take actions, and make choices, with a single tap.

## Default

=== "Design"

    ![Icon Button](/assets/images/component/action/icon_button.png){ loading=lazy }

=== "Implementation"

    ``` dart
    ElevatedButtonIcon(
        onPressed: () {},
        backgroundColor: AppColors.green,
        icon: const Icon(Icons.add),
        tooltip: 'Add',
    ),
    ```
    Change the button type, for example `ElevatedButtonIcon` and `OutlinedButtonIcon`. 
    If you want to use an icon button without a background color, you can use `IconButton`.

    ``` dart
    IconButton(
        onPressed: () {},
        icon: const Icon(Icons.add),
    ),
    ```

## Icon Close Button

=== "Design"

    ![Icon Close Button](/assets/images/component/action/icon_button-close.png){ loading=lazy }

=== "Implementation"

    ``` dart
    IconCloseButton(
        onPressed: () {},
    ),
    ```

    !!! info
        `IconCloseButton` is usually used for [Dialog](documentation/component/comunication/dialog).
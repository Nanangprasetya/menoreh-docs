# Snackbars

Snackbars provide brief messages about app processes at the bottom of the screen.

=== "Design"

    **Snackbar Mobile**

    ![Snackbar mobile](/assets/images/component/comunication/snackbar_mobile.png){ loading=lazy }

    **Snackbar Website**

    ![Snackbar website](/assets/images/component/comunication/snackbar_web.png){ loading=lazy }

=== "Implementation"

    ``` dart
    Fluttertoast.showToast(
        msg: 'This item already exist',
        toastLength: Toast.LENGTH_SHORT,
    );
    ```

    !!! info "To cancel all the toasts call"
        ``` dart
        Fluttertoast.cancel();
        ```

## Support Packages

!!! info
    The Menorah library uses the `fluttertoast` package to call `snackbar`.
    For more can be learned in [Pub Dev](https://pub.dev/packages/fluttertoast).

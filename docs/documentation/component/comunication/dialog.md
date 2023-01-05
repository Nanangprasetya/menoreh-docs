# Dialog

Dialogs inform users about a task and can contain critical information, require decisions, or involve multiple tasks.

## Confirm

=== "Design"

    **Dialog confirm default**

    ![Dialog Confirm](/assets/images/component/comunication/dialog_confirm.png){ loading=lazy }

    **Useing Properties `content`**
    
    ![Dialog Confirm with content](/assets/images/component/comunication/dialog_confirm-content.png){ loading=lazy }

=== "Implementation"

    **Dialog confirm default**
    ``` dart
    AppDialog.confirm(
        context: context,
        title: 'Dialog Title',
        description: 'Phasellus consectetur facilisis',
        submitted: 'Yes',
        onSubmitted: () {},
    ),
    ```

    **Useing Properties `content`**
    ``` dart
    AppDialog.confirm(
        context: context,
        title: 'Change roles',
        description: 'Are you sure you want to change the role for user Nanang?',
        content:  TextFieldDropdown(
            onChanged: (String value) {},
            hint: 'Select Role',
            selectedItem: 'Manager',
            items: const ['Admin', 'Manager', 'User'],
        ),
        submitted: 'Save',
        onSubmitted: () {},
    )
    ```

    !!! info "Constructors"
        - `content` Defines the the Widget on below `description`
        - `submitted` Defines the text for the button submit.
        - `back` Defines the text for the button cancel.
        - `isDismiss` If `false` the dialog cannot be closed.
        - `submittedColor` Defines the color for the button submit.

## Detail

=== "Design"

    ![Dialog Detail](/assets/images/component/comunication/dialog_detail.png){ loading=lazy }

=== "Implementation"

    ``` dart
    AppDialog.detail(
      context: context,
      title: 'Detail User',
      imageUrl: AppImages.avatarUrl,
      content: const [TypeFilterForm()],
      onSubmitted: () {},
      onReset: () {},
    )
    ```

    !!! info "Constructors"
        - `content` put [ListRowBasic] inside these properties.
        - `imageUrl` put url address image type `String`
        - `onDelete` If the property is `null` then the delete button is hidden.
        - `onSubmitted` If the property is `null` then the edit button is hidden.
        - `isDismiss` If `false` the dialog cannot be closed.
        - `heightReduce` set height Dialog `(Height Screen / 1.2) - heightReduce`

## Form

=== "Design"

    ![Dialog Form](/assets/images/component/comunication/dialog_form.png){ loading=lazy }

=== "Implementation"

    ``` dart
    AppDialog.form(
      context: context,
      title: 'Create new Type',
      content: const TypeAddForm(),
      onSubmitted: () {},
    )
    ```

    !!! info "Constructors"
        - `content` put List Form input on the properties
        - `isDismiss` If `false` the dialog cannot be closed.
        - `heightReduce` set height Dialog `(Height Screen / 1.2) - heightReduce`

## Filter

=== "Design"

    ![Dialog Filter](/assets/images/component/comunication/dialog_filter.png){ loading=lazy }

=== "Implementation"

    ``` dart
    AppDialog.filter(
      context: context,
      title: 'Fitler Type',
      content: const TypeFilterForm(),
      onSubmitted: () {},
      onReset: () {},
    )
    ```

    !!! info "Constructors"
        - `content` put List Form input on the properties
        - `isDismiss` If `false` the dialog cannot be closed.
        - `heightReduce` set height Dialog `(Height Screen / 1.2) - heightReduce`

## Import

=== "Design"

    ![Dialog Import](/assets/images/component/comunication/dialog_import.png){ loading=lazy }

=== "Implementation"

    ``` dart
    AppDialog.import(
      context: context,
      title: 'Import kartu',
      description: 'Silahkan masukukan file Excel ke sini. Pastikan data sesuai dengan template.',
      content: TextFieldPicker(
        fileType: FileType.media,
        onDone: (i) {},
      ),
      onSubmitted: () {},
      onDownload: () {},
    ),
    ```

    !!! info "Constructors"
        - `content` put the Widget `TextFieldPicker`
        - `isDismiss` If `false` the dialog cannot be closed.

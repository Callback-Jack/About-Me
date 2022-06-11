# Basic About Me

For this exercise, we need to:

- Create the AboutMe app.
- Add a `TextView` to the layout to display your name.
- Add an `ImageView`.
- Add a `ScrollView` to display scrollable text.
- Add an `EditText` so the user can enter text.\
- Add a `Button` and implement its click handler.

Key points to learn:

- A `ViewGroup` is a view that can contain other views. `LinearLayout` and `ScrollView` are view
  groups.
- `LinearLayout` is a view group that arranges its child views horizontally or vertically.
- Use a `ScrollView` when you need to display content on the screen, such as long text or a
  collection of images. A scroll view can contain only one child view. If you want to scroll more
  than one view, then add a `ViewGroup` such as a `LinearLayout` to the `ScrollView`, and put the
  views to be scrolled inside that `ViewGroup`.
- The *Layout Editor* is a visual design editor inside Android Studio. You can use the Layout Editor
  to build your app's layout by dragging UI elements into the layout.
- A *style* is a collection of attributes that specify the appearance for a view. For example, a
  style can specify font color, font size, background color, padding, and margin.
- You can extract and collect all the formatting of a view into a style. To give your app a
  consistent look, reuse the style for other views.
- `EditText` is a UI element that lets the user enter and modify text.
- A `Button` is a UI element that the user can tap to perform an action. A button can consist of
  text, an icon, or both text and an icon.

- Click listeners
    - You can make any `View` respond to being tapped by adding a click listener to it.
    - The function that defines the click listener receives the `View` that is clicked.
    - You can attach a click-listener function to a `View` in either of two ways:
        - In the XML layout, add the `android:onClick` attribute to the `<View>` element.
        - Programmatically, use the `setOnClickListener(View.OnClickListener)` function in the
          corresponding `Activity`.

- Data Binding and findViewById
    - `findViewById` is a costly operation because it traverses the view hierarchy every time it is
      called.
    - With data binding enabled, the compiler creates references to all views in a `<layout>` that
      have an id, and gathers them in a Binding object.
    - In your code, you create an instance of the binding object, and then reference views through the binding object with no extra overhead.

- Data Binding Views and Data
    - Updating data and then updating the data displayed in views is cumbersome and a source of
      errors. Keeping the data in the view also violates separation of data and presentation.
    - Data binding solves both of these problems. You keep data in a data class. You add a `<data>`
      block to the `<layout>` to identify the data as variables to use with the views. Views
      reference the variables.
    - The compiler generates a binding object that binds the views and data.
    - In your code, you reference and update the data through the binding object, which updates the
      data, and thus what is displayed in the view.
    - Binding views to data sets a foundation for more advanced techniques using data binding.
# hashtagable

Widget and function to implement hashtag-decorated EditableText and RichText.

It decorates the words which starts with "#"

## Usage

- editableText
If you want to decorate input text, `HashTagEditableText` will help you.
```dart
    HashTagEditableText(
      controller: _textEditingController,
      cursorColor: Theme.of(context).cursorColor,
      basicStyle: TextStyle(fontSize: 14,color:Colors.black),
      focusNode: FocusNode(),
      onChanged: (_) {},
      onSubmitted: (_) {},
      decoratedStyle: TextStyle(fontSize: 14,color:Colors.red),
    ),
```

- RichText
If you want to decorate the text only to display, `getHashTagTextSpan()` will help you.
All you need is just putting this function in `RichText`.
```dart
    RichText(
      text: getHashTagTextSpan(
          decoratedStyle: TextStyle(fontSize: 14,color:Colors.red),
          basicStyle: TextStyle(fontSize: 14,color:Colors.black),
          source: "#Hello world. Hello #world",
          onTap: (String text) {
            print(text);
          },
      ),
    ),
```
The argument `onTap(String)` is called when user tapped tagged text.



# Emoji picker for Angular

This project was forked from the [EmojiPanel](https://github.com/danbovey/EmojiPanel) project created by [DanBovey](https://github.com/danbovey)

It's pretty basic right now, not very customizable but propagates necessary emoji selection events and comes with basic search and category selection functionalities.

[Demo](https://lsharir.github.io/angular2-emoji-picker/)


###Usage:

```
import { EmojiPickerModule } from 'angular-emoji-picker';

@NgModule({
  ...
  imports: [
    EmojiPickerModule.forRoot()
  ],
  ...
})
export class AppModule {}

```

###Directive API:

```
<i
    (click)="toggled = !toggled"
    [(emojiPickerIf)]="toggled"
    [emojiPickerPosition]="'bottom' || 'top' || 'left' || 'right'"
    (emojiPickerSelect)="handleSelection($event)">😄</i>
```

### Emitter `(emojiPickerSelect)="handleSelection($event)"`

```
$event = ["😌", "relieved"]
```

### Emitter `(emojiPickerCaretEmitter)="handleCaretChange($event)"`

```
$event = { caretOffset: 13, caretRange: Range{...} }
```

Emoji Picker will get placed relative the element chosen via the directive api, centered and within window borders

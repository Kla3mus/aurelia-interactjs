# aurelia-interactjs

Aurelia plugin to use the [interact.js](http://interactjs.io/) library.

# Generic attributes
Each attribute can be supplied with custom options that will be pased to interactjs, see the interactjs documentation for the options http://interactjs.io/docs/#action-options

## Usage:
```html
<div interact-draggable.bind="options" />
```

Each event can be used in the following way:

```html
<div interact-draggable interact-dragmove.delegate="func($event)" />
```

```javascript
export class Home {
  public func(customEvent: CustomEvent) {
    let event = customEvent.detail;
    console.log("event", event);
  }
}
```

## interact-draggable
The following attributes can be set to catch events

| Attribute                 | Interact.js event |
| ------------------------- | ----------------- |
| interact-dragstart        | dragstart         |
| interact-dragmove         | dragmove          |
| interact-draginertiastart | draginertiastart  |
| interact-dragend          | dragend           |

## interact-dropzone

| Attribute                 | Interact.js event |
| ------------------------- | ----------------- |
| interact-dropactivate     | dropactivate      |
| interact-dragenter        | dragenter         |
| interact-dragleave        | dragleave         |
| interact-drop             | drop              |
| interact-dropdeactivate   | dropdeactivate    |

## interact-gesturable

| Attribute                 | Interact.js event |
| ------------------------- | ----------------- |
| interact-gesturestart     | gesturestart      |
| interact-gesturemove      | gesturemove       |
| interact-gestureend       | gestureend        |

## interact-resizable

| Attribute                   | Interact.js event  |
| --------------------------- | ------------------ |
| interact-resizestart        | resizestart        |
| interact-dragenter          | resizemove         |
| interact-resizeinertiastart | resizeinertiastart |
| interact-resizeend          | resizeend          |

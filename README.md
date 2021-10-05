# swe_intern_test

These files are used to confirm whethere the DevTools' WebSocket can receive all of the data.

## How to Use

### Get dataURL from pictures

1. Open [make_dataURL.html](https://github.com/shihonoda/swe_intern_test/blob/main/make_dataURL.html) on the browser.
2. Open a picture you like.
3. Open the console of DevTools.
4. The dataURL is displayed on the console.

### Testing

1. Open your browser by using port number `9222`.
2. You can get the URL like `ws://127.0.0.1:9222/devtools/browser/...` and copy it.
3. Chenge the URL inside `new WebSocket()` of L16 in [test_fragmented_message.html](https://github.com/shihonoda/swe_intern_test/blob/main/test_fragmented_message.html) to it you got.
4. Change `value` of the method `'DOM.setAttributeValue'`(L64) to the dataURL you got.
5. Open [test_fragmented_message.html](https://github.com/shihonoda/swe_intern_test/blob/main/test_fragmented_message.html) on your browser.
6. If the server succeeded to receive all of the data, the picture will appear on the browser page.
7. You can check the log on the console of DevTools.

To replace newline with colon newline in vim do this:
  ```:%s/\n/,\r/gc```

vim will convert ```\r``` to ```0x0a``` in the text

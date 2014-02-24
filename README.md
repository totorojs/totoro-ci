![totoro](https://f.cloud.github.com/assets/340282/891339/657d9018-fa54-11e2-9760-6955388fd8fc.jpg)

# tci

Continuous integration of totoro.

---

## What is ci config file?

```
[
  {
    "group": "Arale",
    "name": "base",
    "runner": "http://aralejs.org/base/tests/runner.html"
    "email": "lifesinger@gmail.com"
  },
  {
    "group": "Arale",
    "name": "class",
    "runner": "http://aralejs.org/class/tests/runner.html"
    "email": ["lifesinger@gmail.com", "popmore@gmail.com"]
  }
]
```

### All repeated config could be written once

```
{
  "group": "Arale",
  "notice": 1,        // undefined: notice when test finished
                      // 0: notice when test succeeded
                      // 1: notice when test failed
  "tests": [
    {
      "name": "base",
      "runner": "http://aralejs.org/base/tests/runner.html"
      "email": "lifesinger@gmail.com"
    },
    {
      "name": "class",
      "runner": "http://aralejs.org/class/tests/runner.html"
      "email": ["lifesinger@gmail.com", "popmore@gmail.com"]
    }
  ]
}
```
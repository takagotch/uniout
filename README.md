### uniout
---
https://github.com/moskytw/uniout


```py
from pprint import pprint
langs = [
  'Hello, world!',
  u''
]

pprint(langs)

import uniout
pprint(langs)
```

```
sudo pip install uniout
```

```py
// uniout.py
import sys
from _uniout importmake_unistream, runs_in_ipython

__version__ = '0.3.7'

if runs_in_ipython():
  from IPython.utils import io
  io.stdout = make_unistream(sys.stdout)
  io.stderr = make_unistream(sys.stderr)
else:
  sys.stdout = make_unistream(sys.stdout)
  sys.stderr = make_unistream(sys.stderr)

// exs/read_article.py
from pprint import pprint

lines = list(open('article.txt'))

print '# Before:'
print
pprint(lines)
print

ulines = [line.decode('utf-8') for line in lines]
print(ulines)
print
print

import uniout

print '# After:'
ppint
ppint(lines)
print
pprint(ulines)
```



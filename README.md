## Example
```dart
import 'dart:async';
import 'package:stanford_corenlp_dart/stanford_corenlp_dart.dart';

void main() {
  StanfordCoreNLP sfCore = new StanfordCoreNLP('stanford-corenlp', ['tokenize', 'ssplit', 'pos', 'lemma', 'parse'], 6);
  Future ready = sfCore.run();
  ready.then((e) => sfCore.process('Dart is a new platform for scalable web app engineering.').onData((String result) => print(result)));
}
```

## API
### StanfordCoreNLP
StanfordCoreNLP constructor takes two required parameters and one optional.
`_coreNlpPath`: Path to Stanford CoreNLP directory 
`_annotators`: A list of Stanford CoreNLP annotators
`_javaHeapSize`: Java heap size (default = 3)

```dart
StanfordCoreNLP(this._coreNlpPath, this._annotators, [this._javaHeapSize = 3])
```
## License
Copyright (c) 2013, Nawaf Alsallami
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
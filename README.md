## aui-perf nightly record

_44 points · 2026-09-03T05:27:14.273Z to 2026-11-22T12:43:17.069Z · latest runner: Intel(R) Xeon(R) 6975P-C · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 537.14µs | -14.7% | -14.7% ⚠︎ | 537.14µs | 844.63µs | 3 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 795.39µs | +12.0% | +12.0% ⚠︎ | 795.39µs | 1.233ms | 3 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 31.64µs | -9.4% | -9.4% | 31.64µs | 53.36µs | 3 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 353.10µs | -8.6% | -8.6% | 353.10µs | 603.24µs | 3 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 5.538ms | -8.6% | -8.6% | 5.538ms | 9.296ms | 3 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 152.17µs | -3.6% | -3.6% | 152.17µs | 264.69µs | 3 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.379ms | -4.2% | -4.2% | 1.379ms | 2.363ms | 3 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 5.511ms | -4.3% | -4.3% | 5.511ms | 9.243ms | 3 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 6.22µs | -8.0% | -8.0% | 6.22µs | 9.53µs | 3 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 52.48µs | -4.1% | -4.1% | 52.48µs | 85.36µs | 3 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 205.88µs | -4.3% | -4.3% | 205.88µs | 339.32µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 54.34µs |  |  | 54.34µs | 136.51µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 30.35µs |  |  | 30.35µs | 80.22µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 30.88µs |  |  | 30.88µs | 82.46µs | 3 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 194.62µs |  |  | 194.62µs | 310.45µs | 3 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 44.00µs | +24.4% | +24.4% ⚠︎ | 44.00µs | 74.62µs | 3 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 459.77µs | +32.9% | +32.9% ⚠︎ | 459.77µs | 664.05µs | 3 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 6.12µs | +32.3% | +32.3% ⚠︎ | 6.12µs | 9.67µs | 3 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 51.24µs | +32.6% | +32.6% ⚠︎ | 51.24µs | 81.76µs | 3 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 440.36µs | -17.9% | -17.9% ⚠︎ | 440.36µs | 752.62µs | 3 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 3.686ms | -23.3% | -23.3% ⚠︎ | 3.686ms | 5.940ms | 3 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 14.448ms | -24.6% | -24.6% ⚠︎ | 14.448ms | 23.219ms | 3 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 100 parts | 2.407ms |  |  | 2.407ms | 4.009ms | 3 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 2000 parts | 61.185ms |  |  | 61.185ms | 105.431ms | 3 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 500 parts | 11.878ms |  |  | 11.878ms | 17.818ms | 3 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 204.11µs | -38.6% | -38.6% ⚠︎ | 204.11µs | 339.54µs | 3 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 1.969ms | -36.3% | -36.3% ⚠︎ | 1.969ms | 3.209ms | 3 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 7.904ms | -36.9% | -36.9% ⚠︎ | 7.904ms | 12.690ms | 3 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 195.84µs |  |  | 195.84µs | 272.88µs | 3 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.299ms |  |  | 1.299ms | 1.972ms | 3 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 41.45µs | +47.7% | +47.7% ⚠︎ | 41.45µs | 69.37µs | 3 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 414.66µs | +33.3% | +33.3% ⚠︎ | 414.66µs | 696.68µs | 3 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.245ms | +35.1% | +35.1% ⚠︎ | 2.245ms | 3.698ms | 3 |
| external-message-conversion › core: external message tool results › 100 matches | 53.55µs | +59.2% | +59.2% ⚠︎ | 53.55µs | 78.74µs | 3 |
| external-message-conversion › core: external message tool results › 1000 matches | 526.33µs | +53.7% | +53.7% ⚠︎ | 526.33µs | 796.72µs | 3 |
| external-message-conversion › core: external message tool results › 5000 matches | 2.803ms | +52.9% | +52.9% ⚠︎ | 2.803ms | 4.162ms | 3 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 27.41µs | +35.1% | +35.1% ⚠︎ | 27.41µs | 43.65µs | 3 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 260.01µs | +30.8% | +30.8% ⚠︎ | 260.01µs | 428.63µs | 3 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.414ms | +31.4% | +31.4% ⚠︎ | 1.414ms | 2.255ms | 3 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.17µs | +67.1% | +67.1% ⚠︎ | 0.17µs | 0.27µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.30µs | +49.7% | +49.7% ⚠︎ | 0.30µs | 0.47µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 1.57µs | +30.7% | +30.7% ⚠︎ | 1.57µs | 2.44µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.38µs | +6.5% | +6.5% | 0.38µs | 0.65µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.24µs | +28.9% | +28.9% ⚠︎ | 2.24µs | 3.49µs | 3 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 20.41µs | +31.3% | +31.3% ⚠︎ | 20.41µs | 31.99µs | 3 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 110.82µs | +47.8% | +47.8% ⚠︎ | 110.82µs | 142.82µs | 3 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 623.93µs | +30.1% | +30.1% ⚠︎ | 593.59µs | 801.48µs | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 1.931ms | +67.7% | +67.7% ⚠︎ | 1.931ms | 2.801ms | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 118.28µs | +20.4% | +20.4% ⚠︎ | 118.28µs | 206.84µs | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.542ms | +72.5% | +72.5% ⚠︎ | 2.542ms | 3.774ms | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 336.61µs | +55.3% | +55.3% ⚠︎ | 336.61µs | 510.77µs | 3 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 492.20µs | +54.2% | +54.2% ⚠︎ | 492.20µs | 707.61µs | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 5.782ms | +90.8% | +90.8% ⚠︎ | 5.782ms | 7.927ms | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 483.72µs | +4.2% | +4.2% | 483.72µs | 932.58µs | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 14.191ms | +50.8% | +50.8% ⚠︎ | 14.191ms | 24.635ms | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.282ms | +48.8% | +48.8% ⚠︎ | 2.282ms | 3.722ms | 3 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.742ms | +53.5% | +53.5% ⚠︎ | 1.742ms | 2.766ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 1.958ms | +86.9% | +86.9% ⚠︎ | 1.958ms | 3.075ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.194ms | +52.1% | +52.1% ⚠︎ | 2.194ms | 3.364ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 13.364ms | +79.0% | +79.0% ⚠︎ | 13.364ms | 21.826ms | 3 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 14.669ms | +67.8% | +67.8% ⚠︎ | 14.669ms | 23.291ms | 3 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.117ms | +80.6% | +80.6% ⚠︎ | 1.014ms | 1.483ms | 3 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 1.850ms | +69.8% | +69.8% ⚠︎ | 1.850ms | 3.032ms | 3 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 6.336ms | +46.0% | +46.0% ⚠︎ | 6.336ms | 9.876ms | 3 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.391ms | +23.2% | +23.2% ⚠︎ | 1.211ms | 1.391ms | 3 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.395ms | +30.2% | +30.2% ⚠︎ | 1.395ms | 1.959ms | 3 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 3.654ms | +39.3% | +39.3% ⚠︎ | 3.654ms | 5.137ms | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 185.12µs | +53.2% | +53.2% ⚠︎ | 185.12µs | 313.73µs | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 1.535ms | +39.6% | +39.6% ⚠︎ | 1.535ms | 2.582ms | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 180.812ms | +24.3% | +24.3% ⚠︎ | 180.812ms | 291.831ms | 3 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 7.668ms | +41.9% | +41.9% ⚠︎ | 7.668ms | 12.373ms | 3 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.18µs | +13.6% | +13.6% ⚠︎ | 1.18µs | 2.22µs | 3 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 5.39µs | -12.0% | -12.0% ⚠︎ | 5.39µs | 9.28µs | 3 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 25.95µs | +14.0% | +14.0% ⚠︎ | 25.95µs | 39.29µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 4.70µs | +77.6% | +77.6% ⚠︎ | 4.70µs | 6.42µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 15.29µs | +30.3% | +30.3% ⚠︎ | 15.29µs | 20.91µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 45.73µs | +80.6% | +80.6% ⚠︎ | 45.73µs | 62.67µs | 3 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 194.78µs | -21.7% | -21.7% ⚠︎ | 194.78µs | 273.80µs | 3 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.188ms | +87.9% | +87.9% ⚠︎ | 4.188ms | 6.773ms | 3 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 23.853ms | +56.6% | +56.6% ⚠︎ | 23.853ms | 46.010ms | 3 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 309.186ms | +31.5% | +31.5% ⚠︎ | 309.186ms | 466.148ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 367.88µs | +79.9% | +79.9% ⚠︎ | 367.88µs | 642.57µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 621.53µs | +74.5% | +74.5% ⚠︎ | 621.53µs | 916.28µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 2.767ms | +67.2% | +67.2% ⚠︎ | 2.767ms | 3.625ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 338.96µs | +57.6% | +57.6% ⚠︎ | 338.96µs | 610.83µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.173ms | +86.3% | +86.3% ⚠︎ | 1.130ms | 1.454ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 7.927ms | +45.3% | +45.3% ⚠︎ | 7.927ms | 12.000ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 325.86µs | +68.7% | +68.7% ⚠︎ | 325.86µs | 576.39µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 864.06µs | +132.5% | +132.5% ⚠︎ | 805.82µs | 1.135ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.324ms | +60.5% | +60.5% ⚠︎ | 5.324ms | 7.362ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 141.57µs | +48.3% | +48.3% ⚠︎ | 141.57µs | 307.43µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 337.74µs | +67.7% | +67.7% ⚠︎ | 337.74µs | 534.94µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.225ms | +63.3% | +63.3% ⚠︎ | 2.225ms | 2.993ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 10.77µs | +54.0% | +54.0% ⚠︎ | 10.77µs | 23.83µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 22.28µs | +49.9% | +49.9% ⚠︎ | 22.28µs | 39.66µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 186.82µs | +75.0% | +75.0% ⚠︎ | 186.82µs | 262.48µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 399.18µs | +118.0% | +118.0% ⚠︎ | 399.18µs | 658.98µs | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 889.72µs | +129.8% | +129.8% ⚠︎ | 812.00µs | 1.098ms | 3 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 5.498ms | +92.3% | +92.3% ⚠︎ | 5.498ms | 7.121ms | 3 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 153.00µs | +9.0% | +9.0% | 153.00µs | 250.45µs | 3 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.390ms | +9.4% | +9.4% | 1.390ms | 2.151ms | 3 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 704.71µs | +8.5% | +8.5% | 704.71µs | 1.081ms | 3 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 171.42µs | -27.4% | -27.4% ⚠︎ | 171.42µs | 307.87µs | 3 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 1.503ms | -26.9% | -26.9% ⚠︎ | 1.503ms | 2.535ms | 3 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 762.41µs | -26.9% | -26.9% ⚠︎ | 762.41µs | 1.290ms | 3 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 241.67µs | +68.4% | +68.4% ⚠︎ | 241.67µs | 350.32µs | 3 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 16.459ms | +23.5% | +23.5% ⚠︎ | 16.459ms | 25.881ms | 3 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 623.813ms | +90.7% | +90.7% ⚠︎ | 472.059ms | 668.294ms | 3 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 127.31µs | -39.7% | -39.7% ⚠︎ | 127.31µs | 233.93µs | 3 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.043ms | -41.1% | -41.1% ⚠︎ | 1.043ms | 1.827ms | 3 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 527.02µs | -41.1% | -41.1% ⚠︎ | 527.02µs | 936.55µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 142.44µs |  |  | 142.44µs | 208.09µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 675.07µs |  |  | 675.07µs | 939.43µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 154.01µs |  |  | 154.01µs | 229.60µs | 3 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 726.58µs |  |  | 726.58µs | 1.013ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.210ms | +47.7% | +47.7% ⚠︎ | 2.210ms | 3.543ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.260ms | +51.6% | +51.6% ⚠︎ | 2.260ms | 3.540ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.168ms | +51.3% | +51.3% ⚠︎ | 2.168ms | 3.499ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.135ms | +48.6% | +48.6% ⚠︎ | 2.135ms | 3.670ms | 3 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.422ms | +60.2% | +60.2% ⚠︎ | 1.422ms | 2.204ms | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.108ms | +50.1% | +50.1% ⚠︎ | 2.108ms | 3.353ms | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.038ms | +49.2% | +49.2% ⚠︎ | 2.038ms | 3.339ms | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 174.22µs | +40.0% | +40.0% ⚠︎ | 174.22µs | 235.74µs | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 94.03µs | +50.9% | +50.9% ⚠︎ | 94.03µs | 145.22µs | 3 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.112ms | +54.4% | +54.4% ⚠︎ | 1.112ms | 1.723ms | 3 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.201ms | +61.9% | +61.9% ⚠︎ | 1.201ms | 1.976ms | 3 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.301ms | +73.0% | +73.0% ⚠︎ | 1.301ms | 2.094ms | 3 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 29.17µs | +34.4% | +34.4% ⚠︎ | 29.17µs | 53.05µs | 3 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 31.77µs | +44.6% | +44.6% ⚠︎ | 31.77µs | 53.68µs | 3 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 43.95µs | +27.8% | +27.8% ⚠︎ | 43.95µs | 70.17µs | 3 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 983.31µs | +52.6% | +52.6% ⚠︎ | 983.31µs | 1.551ms | 3 |

informational; points come from different runners of the same class, so read trends, not single deltas.

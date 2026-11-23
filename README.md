## aui-perf nightly record

_45 points · 2026-09-03T05:27:14.273Z to 2026-11-23T14:45:19.237Z · latest runner: AMD EPYC 9V74 80-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 705.70µs | +12.0% | +12.0% ⚠︎ | 537.14µs | 844.63µs | 4 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 1.034ms | +45.6% | +45.6% ⚠︎ | 795.39µs | 1.233ms | 4 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 44.57µs | +27.6% | +27.6% ⚠︎ | 31.64µs | 53.36µs | 4 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 506.14µs | +31.0% | +31.0% ⚠︎ | 353.10µs | 603.24µs | 4 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 7.868ms | +29.8% | +29.8% ⚠︎ | 5.538ms | 9.296ms | 4 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 215.58µs | +36.6% | +36.6% ⚠︎ | 152.17µs | 264.69µs | 4 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 2.040ms | +41.7% | +41.7% ⚠︎ | 1.379ms | 2.363ms | 4 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 7.828ms | +36.0% | +36.0% ⚠︎ | 5.511ms | 9.243ms | 4 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 8.39µs | +24.1% | +24.1% ⚠︎ | 6.22µs | 9.53µs | 4 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 70.54µs | +28.9% | +28.9% ⚠︎ | 52.48µs | 85.36µs | 4 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 273.56µs | +27.1% | +27.1% ⚠︎ | 205.88µs | 339.32µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 83.95µs |  |  | 54.34µs | 136.51µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 46.09µs |  |  | 30.35µs | 80.22µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 43.93µs |  |  | 30.88µs | 82.46µs | 4 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 260.31µs |  |  | 194.62µs | 310.45µs | 4 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 54.77µs | +54.9% | +54.9% ⚠︎ | 44.00µs | 74.62µs | 4 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 540.02µs | +56.0% | +56.0% ⚠︎ | 459.77µs | 664.05µs | 4 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 7.70µs | +66.3% | +66.3% ⚠︎ | 6.12µs | 9.67µs | 4 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 62.71µs | +62.3% | +62.3% ⚠︎ | 51.24µs | 81.76µs | 4 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 597.85µs | +11.4% | +11.4% ⚠︎ | 440.36µs | 752.62µs | 4 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 5.152ms | +7.3% | +7.3% | 3.686ms | 5.940ms | 4 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 20.413ms | +6.5% | +6.5% | 14.448ms | 23.219ms | 4 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 100 parts | 3.064ms |  |  | 2.407ms | 4.009ms | 4 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 2000 parts | 104.054ms |  |  | 61.185ms | 105.431ms | 4 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 500 parts | 15.954ms |  |  | 11.878ms | 17.818ms | 4 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 293.64µs | -11.7% | -11.7% ⚠︎ | 204.11µs | 339.54µs | 4 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 2.901ms | -6.2% | -6.2% | 1.969ms | 3.209ms | 4 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 11.320ms | -9.6% | -9.6% | 7.904ms | 12.690ms | 4 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 225.69µs |  |  | 195.84µs | 272.88µs | 4 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.609ms |  |  | 1.299ms | 1.972ms | 4 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 50.64µs | +80.5% | +80.5% ⚠︎ | 41.45µs | 69.37µs | 4 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 512.58µs | +64.8% | +64.8% ⚠︎ | 414.66µs | 696.68µs | 4 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.721ms | +63.8% | +63.8% ⚠︎ | 2.245ms | 3.698ms | 4 |
| external-message-conversion › core: external message tool results › 100 matches | 60.64µs | +80.2% | +80.2% ⚠︎ | 53.55µs | 78.74µs | 4 |
| external-message-conversion › core: external message tool results › 1000 matches | 612.37µs | +78.8% | +78.8% ⚠︎ | 526.33µs | 796.72µs | 4 |
| external-message-conversion › core: external message tool results › 5000 matches | 3.185ms | +73.8% | +73.8% ⚠︎ | 2.803ms | 4.162ms | 4 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 32.26µs | +59.0% | +59.0% ⚠︎ | 27.41µs | 43.65µs | 4 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 304.90µs | +53.4% | +53.4% ⚠︎ | 260.01µs | 428.63µs | 4 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.630ms | +51.4% | +51.4% ⚠︎ | 1.414ms | 2.255ms | 4 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.22µs | +108.8% | +108.8% ⚠︎ | 0.17µs | 0.27µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.38µs | +86.9% | +86.9% ⚠︎ | 0.30µs | 0.47µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 2.15µs | +78.9% | +78.9% ⚠︎ | 1.57µs | 2.44µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.49µs | +37.6% | +37.6% ⚠︎ | 0.38µs | 0.65µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.53µs | +45.5% | +45.5% ⚠︎ | 2.24µs | 3.49µs | 4 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 23.27µs | +49.7% | +49.7% ⚠︎ | 20.41µs | 31.99µs | 4 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 114.57µs | +52.8% | +52.8% ⚠︎ | 110.82µs | 142.82µs | 4 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 594.69µs | +24.0% | +24.0% ⚠︎ | 593.59µs | 801.48µs | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 2.132ms | +85.1% | +85.1% ⚠︎ | 1.931ms | 2.801ms | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 161.34µs | +64.3% | +64.3% ⚠︎ | 118.28µs | 206.84µs | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.761ms | +87.4% | +87.4% ⚠︎ | 2.542ms | 3.774ms | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 391.18µs | +80.5% | +80.5% ⚠︎ | 336.61µs | 510.77µs | 4 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 504.07µs | +57.9% | +57.9% ⚠︎ | 492.20µs | 707.61µs | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 6.117ms | +101.9% | +101.9% ⚠︎ | 5.782ms | 7.927ms | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 743.52µs | +60.2% | +60.2% ⚠︎ | 483.72µs | 932.58µs | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 16.648ms | +76.9% | +76.9% ⚠︎ | 14.191ms | 24.635ms | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.746ms | +79.0% | +79.0% ⚠︎ | 2.282ms | 3.722ms | 4 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.958ms | +72.6% | +72.6% ⚠︎ | 1.742ms | 2.766ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 2.432ms | +132.1% | +132.1% ⚠︎ | 1.958ms | 3.075ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.613ms | +81.1% | +81.1% ⚠︎ | 2.194ms | 3.364ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 17.157ms | +129.8% | +129.8% ⚠︎ | 13.364ms | 21.826ms | 4 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 18.341ms | +109.8% | +109.8% ⚠︎ | 14.669ms | 23.291ms | 4 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.081ms | +74.8% | +74.8% ⚠︎ | 1.014ms | 1.483ms | 4 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 2.248ms | +106.3% | +106.3% ⚠︎ | 1.850ms | 3.032ms | 4 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 7.938ms | +83.0% | +83.0% ⚠︎ | 6.336ms | 9.876ms | 4 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.262ms | +11.8% | +11.8% ⚠︎ | 1.211ms | 1.391ms | 4 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.561ms | +45.7% | +45.7% ⚠︎ | 1.395ms | 1.959ms | 4 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 4.461ms | +70.0% | +70.0% ⚠︎ | 3.654ms | 5.137ms | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 267.26µs | +121.2% | +121.2% ⚠︎ | 185.12µs | 313.73µs | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 2.213ms | +101.2% | +101.2% ⚠︎ | 1.535ms | 2.582ms | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 215.221ms | +48.0% | +48.0% ⚠︎ | 180.812ms | 291.831ms | 4 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 10.843ms | +100.6% | +100.6% ⚠︎ | 7.668ms | 12.373ms | 4 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.89µs | +81.7% | +81.7% ⚠︎ | 1.18µs | 2.22µs | 4 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 9.96µs | +62.6% | +62.6% ⚠︎ | 5.39µs | 9.96µs | 4 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 38.09µs | +67.3% | +67.3% ⚠︎ | 25.95µs | 39.29µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 6.82µs | +157.8% | +157.8% ⚠︎ | 4.70µs | 6.82µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 20.44µs | +74.2% | +74.2% ⚠︎ | 15.29µs | 20.91µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 72.47µs | +186.3% | +186.3% ⚠︎ | 45.73µs | 72.47µs | 4 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 258.23µs | +3.8% | +3.8% | 194.78µs | 273.80µs | 4 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 5.171ms | +132.1% | +132.1% ⚠︎ | 4.188ms | 6.773ms | 4 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 38.127ms | +150.4% | +150.4% ⚠︎ | 23.853ms | 46.010ms | 4 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 411.613ms | +75.0% | +75.0% ⚠︎ | 309.186ms | 466.148ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 439.05µs | +114.7% | +114.7% ⚠︎ | 367.88µs | 642.57µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 669.87µs | +88.1% | +88.1% ⚠︎ | 621.53µs | 916.28µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 4.348ms | +162.7% | +162.7% ⚠︎ | 2.767ms | 4.348ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 443.01µs | +106.0% | +106.0% ⚠︎ | 338.96µs | 610.83µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.254ms | +99.0% | +99.0% ⚠︎ | 1.130ms | 1.454ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 14.941ms | +174.0% | +174.0% ⚠︎ | 7.927ms | 14.941ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 467.22µs | +141.8% | +141.8% ⚠︎ | 325.86µs | 576.39µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 905.12µs | +143.6% | +143.6% ⚠︎ | 805.82µs | 1.135ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 10.734ms | +223.6% | +223.6% ⚠︎ | 5.324ms | 10.734ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 278.91µs | +192.2% | +192.2% ⚠︎ | 141.57µs | 307.43µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 432.40µs | +114.7% | +114.7% ⚠︎ | 337.74µs | 534.94µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.479ms | +81.9% | +81.9% ⚠︎ | 2.225ms | 2.993ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 14.98µs | +114.2% | +114.2% ⚠︎ | 10.77µs | 23.83µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 27.64µs | +85.9% | +85.9% ⚠︎ | 22.28µs | 39.66µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 210.70µs | +97.4% | +97.4% ⚠︎ | 186.82µs | 262.48µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 502.60µs | +174.5% | +174.5% ⚠︎ | 399.18µs | 658.98µs | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 830.99µs | +114.6% | +114.6% ⚠︎ | 812.00µs | 1.098ms | 4 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 7.954ms | +178.2% | +178.2% ⚠︎ | 5.498ms | 7.954ms | 4 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 202.07µs | +44.0% | +44.0% ⚠︎ | 153.00µs | 250.45µs | 4 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.790ms | +41.0% | +41.0% ⚠︎ | 1.390ms | 2.151ms | 4 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 900.63µs | +38.7% | +38.7% ⚠︎ | 704.71µs | 1.081ms | 4 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 247.83µs | +4.9% | +4.9% | 171.42µs | 307.87µs | 4 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 2.164ms | +5.1% | +5.1% | 1.503ms | 2.535ms | 4 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 1.094ms | +4.8% | +4.8% | 762.41µs | 1.290ms | 4 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 268.05µs | +86.8% | +86.8% ⚠︎ | 241.67µs | 350.32µs | 4 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 21.680ms | +62.7% | +62.7% ⚠︎ | 16.459ms | 25.881ms | 4 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 479.267ms | +46.5% | +46.5% ⚠︎ | 472.059ms | 668.294ms | 4 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 191.46µs | -9.3% | -9.3% | 127.31µs | 233.93µs | 4 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.588ms | -10.3% | -10.3% ⚠︎ | 1.043ms | 1.827ms | 4 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 809.99µs | -9.5% | -9.5% | 527.02µs | 936.55µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 163.47µs |  |  | 142.44µs | 208.09µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 755.23µs |  |  | 675.07µs | 939.43µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 180.18µs |  |  | 154.01µs | 229.60µs | 4 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 805.31µs |  |  | 726.58µs | 1.013ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.804ms | +87.4% | +87.4% ⚠︎ | 2.210ms | 3.543ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.814ms | +88.7% | +88.7% ⚠︎ | 2.260ms | 3.540ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.726ms | +90.2% | +90.2% ⚠︎ | 2.168ms | 3.499ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.744ms | +91.0% | +91.0% ⚠︎ | 2.135ms | 3.670ms | 4 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.747ms | +96.7% | +96.7% ⚠︎ | 1.422ms | 2.204ms | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.567ms | +82.7% | +82.7% ⚠︎ | 2.108ms | 3.353ms | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.550ms | +86.7% | +86.7% ⚠︎ | 2.038ms | 3.339ms | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 203.89µs | +63.8% | +63.8% ⚠︎ | 174.22µs | 235.74µs | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 109.61µs | +75.9% | +75.9% ⚠︎ | 94.03µs | 145.22µs | 4 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.365ms | +89.6% | +89.6% ⚠︎ | 1.112ms | 1.723ms | 4 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.426ms | +92.2% | +92.2% ⚠︎ | 1.201ms | 1.976ms | 4 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.516ms | +101.7% | +101.7% ⚠︎ | 1.301ms | 2.094ms | 4 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 38.43µs | +77.1% | +77.1% ⚠︎ | 29.17µs | 53.05µs | 4 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 40.75µs | +85.4% | +85.4% ⚠︎ | 31.77µs | 53.68µs | 4 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 54.76µs | +59.3% | +59.3% ⚠︎ | 43.95µs | 70.17µs | 4 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 1.150ms | +78.4% | +78.4% ⚠︎ | 983.31µs | 1.551ms | 4 |

informational; points come from different runners of the same class, so read trends, not single deltas.

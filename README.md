## aui-perf nightly record

_46 points · 2026-09-03T05:27:14.273Z to 2026-11-24T15:00:48.093Z · latest runner: Intel(R) Xeon(R) 6975P-C · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 558.56µs | -11.3% | -11.3% ⚠︎ | 537.14µs | 844.63µs | 5 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 833.77µs | +17.4% | +17.4% ⚠︎ | 795.39µs | 1.233ms | 5 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 34.61µs | -0.9% | -0.9% | 31.64µs | 53.36µs | 5 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 369.61µs | -4.4% | -4.4% | 353.10µs | 603.24µs | 5 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 5.807ms | -4.2% | -4.2% | 5.538ms | 9.296ms | 5 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 153.12µs | -3.0% | -3.0% | 152.17µs | 264.69µs | 5 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.421ms | -1.3% | -1.3% | 1.379ms | 2.363ms | 5 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 5.687ms | -1.2% | -1.2% | 5.511ms | 9.243ms | 5 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 6.58µs | -2.7% | -2.7% | 6.22µs | 9.53µs | 5 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 54.65µs | -0.2% | -0.2% | 52.48µs | 85.36µs | 5 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 219.56µs | +2.0% | +2.0% | 205.88µs | 339.32µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 60.25µs |  |  | 54.34µs | 136.51µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 31.07µs |  |  | 30.35µs | 80.22µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 32.60µs |  |  | 30.88µs | 82.46µs | 5 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 207.00µs |  |  | 194.62µs | 310.45µs | 5 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 46.52µs | +31.5% | +31.5% ⚠︎ | 44.00µs | 74.62µs | 5 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 494.13µs | +42.8% | +42.8% ⚠︎ | 459.77µs | 664.05µs | 5 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 6.44µs | +39.1% | +39.1% ⚠︎ | 6.12µs | 9.67µs | 5 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 54.99µs | +42.3% | +42.3% ⚠︎ | 51.24µs | 81.76µs | 5 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 443.69µs | -17.3% | -17.3% ⚠︎ | 440.36µs | 752.62µs | 5 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 3.697ms | -23.0% | -23.0% ⚠︎ | 3.686ms | 5.940ms | 5 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 14.603ms | -23.8% | -23.8% ⚠︎ | 14.448ms | 23.219ms | 5 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 100 parts | 2.783ms |  |  | 2.407ms | 4.009ms | 5 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 2000 parts | 68.580ms |  |  | 61.185ms | 105.431ms | 5 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 500 parts | 12.879ms |  |  | 11.878ms | 17.818ms | 5 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 210.33µs | -36.8% | -36.8% ⚠︎ | 204.11µs | 339.54µs | 5 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 2.070ms | -33.1% | -33.1% ⚠︎ | 1.969ms | 3.209ms | 5 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 8.045ms | -35.7% | -35.7% ⚠︎ | 7.904ms | 12.690ms | 5 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 209.24µs |  |  | 195.84µs | 272.88µs | 5 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.738ms |  |  | 1.299ms | 1.972ms | 5 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 43.27µs | +54.3% | +54.3% ⚠︎ | 41.45µs | 69.37µs | 5 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 432.86µs | +39.2% | +39.2% ⚠︎ | 414.66µs | 696.68µs | 5 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.329ms | +40.2% | +40.2% ⚠︎ | 2.245ms | 3.698ms | 5 |
| external-message-conversion › core: external message tool results › 100 matches | 54.56µs | +62.2% | +62.2% ⚠︎ | 53.55µs | 78.74µs | 5 |
| external-message-conversion › core: external message tool results › 1000 matches | 547.27µs | +59.8% | +59.8% ⚠︎ | 526.33µs | 796.72µs | 5 |
| external-message-conversion › core: external message tool results › 5000 matches | 2.937ms | +60.2% | +60.2% ⚠︎ | 2.803ms | 4.162ms | 5 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 28.42µs | +40.1% | +40.1% ⚠︎ | 27.41µs | 43.65µs | 5 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 275.68µs | +38.7% | +38.7% ⚠︎ | 260.01µs | 428.63µs | 5 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.498ms | +39.2% | +39.2% ⚠︎ | 1.414ms | 2.255ms | 5 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.18µs | +70.4% | +70.4% ⚠︎ | 0.17µs | 0.27µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.30µs | +47.4% | +47.4% ⚠︎ | 0.30µs | 0.47µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 1.58µs | +31.0% | +31.0% ⚠︎ | 1.57µs | 2.44µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.38µs | +7.3% | +7.3% | 0.38µs | 0.65µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.34µs | +34.6% | +34.6% ⚠︎ | 2.24µs | 3.49µs | 5 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 20.17µs | +29.8% | +29.8% ⚠︎ | 20.17µs | 31.99µs | 5 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 115.96µs | +54.6% | +54.6% ⚠︎ | 110.82µs | 142.82µs | 5 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 649.20µs | +35.4% | +35.4% ⚠︎ | 593.59µs | 801.48µs | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 1.998ms | +73.4% | +73.4% ⚠︎ | 1.931ms | 2.801ms | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 119.13µs | +21.3% | +21.3% ⚠︎ | 118.28µs | 206.84µs | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.548ms | +72.9% | +72.9% ⚠︎ | 2.542ms | 3.774ms | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 348.89µs | +61.0% | +61.0% ⚠︎ | 336.61µs | 510.77µs | 5 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 515.92µs | +61.6% | +61.6% ⚠︎ | 492.20µs | 707.61µs | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 5.779ms | +90.8% | +90.8% ⚠︎ | 5.779ms | 7.927ms | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 484.89µs | +4.5% | +4.5% | 483.72µs | 932.58µs | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 15.087ms | +60.4% | +60.4% ⚠︎ | 14.191ms | 24.635ms | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.398ms | +56.4% | +56.4% ⚠︎ | 2.282ms | 3.722ms | 5 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.797ms | +58.4% | +58.4% ⚠︎ | 1.742ms | 2.766ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 1.993ms | +90.3% | +90.3% ⚠︎ | 1.958ms | 3.075ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.207ms | +53.0% | +53.0% ⚠︎ | 2.194ms | 3.364ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 13.552ms | +81.5% | +81.5% ⚠︎ | 13.364ms | 21.826ms | 5 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 14.890ms | +70.4% | +70.4% ⚠︎ | 14.669ms | 23.291ms | 5 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.112ms | +79.9% | +79.9% ⚠︎ | 1.014ms | 1.483ms | 5 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 1.937ms | +77.8% | +77.8% ⚠︎ | 1.850ms | 3.032ms | 5 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 6.689ms | +54.2% | +54.2% ⚠︎ | 6.336ms | 9.876ms | 5 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.396ms | +23.6% | +23.6% ⚠︎ | 1.211ms | 1.396ms | 5 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.438ms | +34.2% | +34.2% ⚠︎ | 1.395ms | 1.959ms | 5 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 3.887ms | +48.1% | +48.1% ⚠︎ | 3.654ms | 5.137ms | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 214.23µs | +77.3% | +77.3% ⚠︎ | 185.12µs | 313.73µs | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 1.816ms | +65.1% | +65.1% ⚠︎ | 1.535ms | 2.582ms | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 184.649ms | +27.0% | +27.0% ⚠︎ | 180.812ms | 291.831ms | 5 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 8.795ms | +62.7% | +62.7% ⚠︎ | 7.668ms | 12.373ms | 5 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.26µs | +21.5% | +21.5% ⚠︎ | 1.18µs | 2.22µs | 5 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 5.43µs | -11.4% | -11.4% ⚠︎ | 5.39µs | 9.96µs | 5 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 25.69µs | +12.8% | +12.8% ⚠︎ | 25.69µs | 39.29µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 4.73µs | +79.0% | +79.0% ⚠︎ | 4.70µs | 6.82µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 15.67µs | +33.5% | +33.5% ⚠︎ | 15.29µs | 20.91µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 46.03µs | +81.8% | +81.8% ⚠︎ | 45.73µs | 72.47µs | 5 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 193.21µs | -22.3% | -22.3% ⚠︎ | 193.21µs | 273.80µs | 5 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.516ms | +102.6% | +102.6% ⚠︎ | 4.188ms | 6.773ms | 5 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 27.389ms | +79.9% | +79.9% ⚠︎ | 23.853ms | 46.010ms | 5 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 336.800ms | +43.2% | +43.2% ⚠︎ | 309.186ms | 466.148ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 418.26µs | +104.5% | +104.5% ⚠︎ | 367.88µs | 642.57µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 638.72µs | +79.3% | +79.3% ⚠︎ | 621.53µs | 916.28µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 3.072ms | +85.6% | +85.6% ⚠︎ | 2.767ms | 4.348ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 415.47µs | +93.2% | +93.2% ⚠︎ | 338.96µs | 610.83µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.127ms | +79.0% | +79.0% ⚠︎ | 1.127ms | 1.454ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 9.195ms | +68.6% | +68.6% ⚠︎ | 7.927ms | 14.941ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 374.42µs | +93.8% | +93.8% ⚠︎ | 325.86µs | 576.39µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 910.36µs | +145.0% | +145.0% ⚠︎ | 805.82µs | 1.135ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.538ms | +66.9% | +66.9% ⚠︎ | 5.324ms | 10.734ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 164.95µs | +72.8% | +72.8% ⚠︎ | 141.57µs | 307.43µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 378.05µs | +87.7% | +87.7% ⚠︎ | 337.74µs | 534.94µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.784ms | +104.3% | +104.3% ⚠︎ | 2.225ms | 2.993ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 11.06µs | +58.2% | +58.2% ⚠︎ | 10.77µs | 23.83µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 23.36µs | +57.1% | +57.1% ⚠︎ | 22.28µs | 39.66µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 203.74µs | +90.9% | +90.9% ⚠︎ | 186.82µs | 262.48µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 432.17µs | +136.1% | +136.1% ⚠︎ | 399.18µs | 658.98µs | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 840.19µs | +117.0% | +117.0% ⚠︎ | 812.00µs | 1.098ms | 5 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 5.888ms | +106.0% | +106.0% ⚠︎ | 5.498ms | 7.954ms | 5 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 158.86µs | +13.2% | +13.2% ⚠︎ | 153.00µs | 250.45µs | 5 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.454ms | +14.5% | +14.5% ⚠︎ | 1.390ms | 2.151ms | 5 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 730.38µs | +12.5% | +12.5% ⚠︎ | 704.71µs | 1.081ms | 5 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 179.81µs | -23.9% | -23.9% ⚠︎ | 171.42µs | 307.87µs | 5 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 1.587ms | -22.9% | -22.9% ⚠︎ | 1.503ms | 2.535ms | 5 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 812.35µs | -22.2% | -22.2% ⚠︎ | 762.41µs | 1.290ms | 5 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 248.76µs | +73.4% | +73.4% ⚠︎ | 241.67µs | 350.32µs | 5 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 17.391ms | +30.5% | +30.5% ⚠︎ | 16.459ms | 25.881ms | 5 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 672.158ms | +105.5% | +105.5% ⚠︎ | 472.059ms | 672.158ms | 5 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 131.68µs | -37.6% | -37.6% ⚠︎ | 127.31µs | 233.93µs | 5 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.079ms | -39.0% | -39.0% ⚠︎ | 1.043ms | 1.827ms | 5 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 548.14µs | -38.8% | -38.8% ⚠︎ | 527.02µs | 936.55µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 157.14µs |  |  | 142.44µs | 208.09µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 735.27µs |  |  | 675.07µs | 939.43µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 171.47µs |  |  | 154.01µs | 229.60µs | 5 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 778.74µs |  |  | 726.58µs | 1.013ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.388ms | +59.6% | +59.6% ⚠︎ | 2.210ms | 3.543ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.492ms | +67.1% | +67.1% ⚠︎ | 2.260ms | 3.540ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.380ms | +66.0% | +66.0% ⚠︎ | 2.168ms | 3.499ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.194ms | +52.7% | +52.7% ⚠︎ | 2.135ms | 3.670ms | 5 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.540ms | +73.4% | +73.4% ⚠︎ | 1.422ms | 2.204ms | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.215ms | +57.7% | +57.7% ⚠︎ | 2.108ms | 3.353ms | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.202ms | +61.3% | +61.3% ⚠︎ | 2.038ms | 3.339ms | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 244.09µs | +96.1% | +96.1% ⚠︎ | 174.22µs | 244.09µs | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 95.40µs | +53.1% | +53.1% ⚠︎ | 94.03µs | 145.22µs | 5 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.180ms | +63.9% | +63.9% ⚠︎ | 1.112ms | 1.723ms | 5 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.294ms | +74.5% | +74.5% ⚠︎ | 1.201ms | 1.976ms | 5 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.345ms | +78.9% | +78.9% ⚠︎ | 1.301ms | 2.094ms | 5 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 31.18µs | +43.7% | +43.7% ⚠︎ | 29.17µs | 53.05µs | 5 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 33.54µs | +52.6% | +52.6% ⚠︎ | 31.77µs | 53.68µs | 5 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 56.07µs | +63.1% | +63.1% ⚠︎ | 43.95µs | 70.17µs | 5 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 978.74µs | +51.9% | +51.9% ⚠︎ | 978.74µs | 1.551ms | 5 |

informational; points come from different runners of the same class, so read trends, not single deltas.

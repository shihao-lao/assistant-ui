## aui-perf nightly record

_47 points · 2026-09-03T05:27:14.273Z to 2026-11-25T14:28:25.857Z · latest runner: AMD EPYC 9V45 96-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 486.04µs | -22.8% | -22.8% ⚠︎ | 486.04µs | 844.63µs | 6 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 732.34µs | +3.1% | +3.1% | 732.34µs | 1.233ms | 6 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 34.39µs | -1.5% | -1.5% | 31.64µs | 53.36µs | 6 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 380.64µs | -1.5% | -1.5% | 353.10µs | 603.24µs | 6 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 5.899ms | -2.7% | -2.7% | 5.538ms | 9.296ms | 6 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 162.63µs | +3.0% | +3.0% | 152.17µs | 264.69µs | 6 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.484ms | +3.1% | +3.1% | 1.379ms | 2.363ms | 6 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 6.025ms | +4.6% | +4.6% | 5.511ms | 9.243ms | 6 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 5.76µs | -14.8% | -14.8% ⚠︎ | 5.76µs | 9.53µs | 6 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 48.18µs | -12.0% | -12.0% ⚠︎ | 48.18µs | 85.36µs | 6 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 187.58µs | -12.8% | -12.8% ⚠︎ | 187.58µs | 339.32µs | 6 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 55.01µs |  |  | 54.34µs | 136.51µs | 6 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 27.53µs |  |  | 27.53µs | 80.22µs | 6 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 30.27µs |  |  | 30.27µs | 82.46µs | 6 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 175.63µs |  |  | 175.63µs | 310.45µs | 6 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 43.89µs | +24.1% | +24.1% ⚠︎ | 43.89µs | 74.62µs | 6 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 449.38µs | +29.9% | +29.9% ⚠︎ | 449.38µs | 664.05µs | 6 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 5.58µs | +20.5% | +20.5% ⚠︎ | 5.58µs | 9.67µs | 6 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 48.34µs | +25.1% | +25.1% ⚠︎ | 48.34µs | 81.76µs | 6 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 401.19µs | -25.2% | -25.2% ⚠︎ | 401.19µs | 752.62µs | 6 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 3.575ms | -25.6% | -25.6% ⚠︎ | 3.575ms | 5.940ms | 6 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 14.053ms | -26.7% | -26.7% ⚠︎ | 14.053ms | 23.219ms | 6 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 100 parts | 2.317ms |  |  | 2.317ms | 4.009ms | 6 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 2000 parts | 67.181ms |  |  | 61.185ms | 105.431ms | 6 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 500 parts | 12.659ms |  |  | 11.878ms | 17.818ms | 6 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 206.66µs | -37.9% | -37.9% ⚠︎ | 204.11µs | 339.54µs | 6 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 1.982ms | -35.9% | -35.9% ⚠︎ | 1.969ms | 3.209ms | 6 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 7.800ms | -37.7% | -37.7% ⚠︎ | 7.800ms | 12.690ms | 6 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 151.34µs |  |  | 151.34µs | 272.88µs | 6 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.001ms |  |  | 1.001ms | 1.972ms | 6 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 35.97µs | +28.2% | +28.2% ⚠︎ | 35.97µs | 69.37µs | 6 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 368.56µs | +18.5% | +18.5% ⚠︎ | 368.56µs | 696.68µs | 6 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 1.978ms | +19.1% | +19.1% ⚠︎ | 1.978ms | 3.698ms | 6 |
| external-message-conversion › core: external message tool results › 100 matches | 40.69µs | +20.9% | +20.9% ⚠︎ | 40.69µs | 78.74µs | 6 |
| external-message-conversion › core: external message tool results › 1000 matches | 417.67µs | +21.9% | +21.9% ⚠︎ | 417.67µs | 796.72µs | 6 |
| external-message-conversion › core: external message tool results › 5000 matches | 2.200ms | +20.1% | +20.1% ⚠︎ | 2.200ms | 4.162ms | 6 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 21.85µs | +7.7% | +7.7% | 21.85µs | 43.65µs | 6 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 206.96µs | +4.1% | +4.1% | 206.96µs | 428.63µs | 6 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.112ms | +3.3% | +3.3% | 1.112ms | 2.255ms | 6 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.16µs | +50.9% | +50.9% ⚠︎ | 0.16µs | 0.27µs | 6 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.27µs | +31.1% | +31.1% ⚠︎ | 0.27µs | 0.47µs | 6 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 1.55µs | +28.8% | +28.8% ⚠︎ | 1.55µs | 2.44µs | 6 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.39µs | +7.8% | +7.8% | 0.38µs | 0.65µs | 6 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 1.75µs | +0.3% | +0.3% | 1.75µs | 3.49µs | 6 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 15.62µs | +0.5% | +0.5% | 15.62µs | 31.99µs | 6 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 97.79µs | +30.4% | +30.4% ⚠︎ | 97.79µs | 142.82µs | 6 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 491.21µs | +2.5% | +2.5% | 491.21µs | 801.48µs | 6 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 1.454ms | +26.2% | +26.2% ⚠︎ | 1.454ms | 2.801ms | 6 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 104.26µs | +6.2% | +6.2% | 104.26µs | 206.84µs | 6 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 1.929ms | +30.9% | +30.9% ⚠︎ | 1.929ms | 3.774ms | 6 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 261.09µs | +20.5% | +20.5% ⚠︎ | 261.09µs | 510.77µs | 6 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 377.90µs | +18.4% | +18.4% ⚠︎ | 377.90µs | 707.61µs | 6 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 3.738ms | +23.4% | +23.4% ⚠︎ | 3.738ms | 7.927ms | 6 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 477.62µs | +2.9% | +2.9% | 477.62µs | 932.58µs | 6 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 11.071ms | +17.7% | +17.7% ⚠︎ | 11.071ms | 24.635ms | 6 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 1.894ms | +23.5% | +23.5% ⚠︎ | 1.894ms | 3.722ms | 6 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.478ms | +30.3% | +30.3% ⚠︎ | 1.478ms | 2.766ms | 6 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 1.582ms | +51.0% | +51.0% ⚠︎ | 1.582ms | 3.075ms | 6 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 1.771ms | +22.8% | +22.8% ⚠︎ | 1.771ms | 3.364ms | 6 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 11.843ms | +58.6% | +58.6% ⚠︎ | 11.843ms | 21.826ms | 6 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 13.098ms | +49.8% | +49.8% ⚠︎ | 13.098ms | 23.291ms | 6 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 863.76µs | +39.7% | +39.7% ⚠︎ | 863.76µs | 1.483ms | 6 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 1.529ms | +40.4% | +40.4% ⚠︎ | 1.529ms | 3.032ms | 6 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 5.695ms | +31.3% | +31.3% ⚠︎ | 5.695ms | 9.876ms | 6 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.163ms | +3.0% | +3.0% | 1.163ms | 1.396ms | 6 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.325ms | +23.7% | +23.7% ⚠︎ | 1.325ms | 1.959ms | 6 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 3.002ms | +14.4% | +14.4% ⚠︎ | 3.002ms | 5.137ms | 6 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 203.96µs | +68.8% | +68.8% ⚠︎ | 185.12µs | 313.73µs | 6 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 1.697ms | +54.3% | +54.3% ⚠︎ | 1.535ms | 2.582ms | 6 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 159.470ms | +9.6% | +9.6% | 159.470ms | 291.831ms | 6 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 8.099ms | +49.8% | +49.8% ⚠︎ | 7.668ms | 12.373ms | 6 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.39µs | +34.3% | +34.3% ⚠︎ | 1.18µs | 2.22µs | 6 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 6.45µs | +5.2% | +5.2% | 5.39µs | 9.96µs | 6 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 19.65µs | -13.7% | -13.7% ⚠︎ | 19.65µs | 39.29µs | 6 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 4.85µs | +83.4% | +83.4% ⚠︎ | 4.70µs | 6.82µs | 6 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 14.27µs | +21.6% | +21.6% ⚠︎ | 14.27µs | 20.91µs | 6 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 47.09µs | +86.0% | +86.0% ⚠︎ | 45.73µs | 72.47µs | 6 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 208.74µs | -16.1% | -16.1% ⚠︎ | 193.21µs | 273.80µs | 6 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 3.619ms | +62.4% | +62.4% ⚠︎ | 3.619ms | 6.773ms | 6 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 25.360ms | +66.5% | +66.5% ⚠︎ | 23.853ms | 46.010ms | 6 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 337.248ms | +43.4% | +43.4% ⚠︎ | 309.186ms | 466.148ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 283.97µs | +38.9% | +38.9% ⚠︎ | 283.97µs | 642.57µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 431.16µs | +21.0% | +21.0% ⚠︎ | 431.16µs | 916.28µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 2.148ms | +29.8% | +29.8% ⚠︎ | 2.148ms | 4.348ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 294.29µs | +36.8% | +36.8% ⚠︎ | 294.29µs | 610.83µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 765.79µs | +21.6% | +21.6% ⚠︎ | 765.79µs | 1.454ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 7.122ms | +30.6% | +30.6% ⚠︎ | 7.122ms | 14.941ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 292.93µs | +51.6% | +51.6% ⚠︎ | 292.93µs | 576.39µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 525.62µs | +41.5% | +41.5% ⚠︎ | 525.62µs | 1.135ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 5.035ms | +51.8% | +51.8% ⚠︎ | 5.035ms | 10.734ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 130.53µs | +36.8% | +36.8% ⚠︎ | 130.53µs | 307.43µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 265.89µs | +32.0% | +32.0% ⚠︎ | 265.89µs | 534.94µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 1.619ms | +18.8% | +18.8% ⚠︎ | 1.619ms | 2.993ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 9.72µs | +39.0% | +39.0% ⚠︎ | 9.72µs | 23.83µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 20.12µs | +35.3% | +35.3% ⚠︎ | 20.12µs | 39.66µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 148.93µs | +39.5% | +39.5% ⚠︎ | 148.93µs | 262.48µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 283.58µs | +54.9% | +54.9% ⚠︎ | 283.58µs | 658.98µs | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 507.71µs | +31.1% | +31.1% ⚠︎ | 507.71µs | 1.098ms | 6 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 4.753ms | +66.3% | +66.3% ⚠︎ | 4.753ms | 7.954ms | 6 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 150.27µs | +7.1% | +7.1% | 150.27µs | 250.45µs | 6 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.332ms | +4.8% | +4.8% | 1.332ms | 2.151ms | 6 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 673.52µs | +3.7% | +3.7% | 673.52µs | 1.081ms | 6 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 181.69µs | -23.1% | -23.1% ⚠︎ | 171.42µs | 307.87µs | 6 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 1.565ms | -24.0% | -24.0% ⚠︎ | 1.503ms | 2.535ms | 6 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 802.29µs | -23.1% | -23.1% ⚠︎ | 762.41µs | 1.290ms | 6 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 193.14µs | +34.6% | +34.6% ⚠︎ | 193.14µs | 350.32µs | 6 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 14.596ms | +9.5% | +9.5% | 14.596ms | 25.881ms | 6 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 407.503ms | +24.6% | +24.6% ⚠︎ | 407.503ms | 672.158ms | 6 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 139.92µs | -33.7% | -33.7% ⚠︎ | 127.31µs | 233.93µs | 6 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.182ms | -33.2% | -33.2% ⚠︎ | 1.043ms | 1.827ms | 6 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 604.93µs | -32.4% | -32.4% ⚠︎ | 527.02µs | 936.55µs | 6 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 104.35µs |  |  | 104.35µs | 208.09µs | 6 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 472.58µs |  |  | 472.58µs | 939.43µs | 6 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 116.70µs |  |  | 116.70µs | 229.60µs | 6 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 516.54µs |  |  | 516.54µs | 1.013ms | 6 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.076ms | +38.8% | +38.8% ⚠︎ | 2.076ms | 3.543ms | 6 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.116ms | +41.9% | +41.9% ⚠︎ | 2.116ms | 3.540ms | 6 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 1.967ms | +37.2% | +37.2% ⚠︎ | 1.967ms | 3.499ms | 6 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 1.957ms | +36.2% | +36.2% ⚠︎ | 1.957ms | 3.670ms | 6 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.254ms | +41.2% | +41.2% ⚠︎ | 1.254ms | 2.204ms | 6 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 1.942ms | +38.3% | +38.3% ⚠︎ | 1.942ms | 3.353ms | 6 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 1.860ms | +36.2% | +36.2% ⚠︎ | 1.860ms | 3.339ms | 6 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 163.90µs | +31.7% | +31.7% ⚠︎ | 163.90µs | 244.09µs | 6 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 85.07µs | +36.5% | +36.5% ⚠︎ | 85.07µs | 145.22µs | 6 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 993.49µs | +38.0% | +38.0% ⚠︎ | 993.49µs | 1.723ms | 6 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.010ms | +36.2% | +36.2% ⚠︎ | 1.010ms | 1.976ms | 6 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.052ms | +40.0% | +40.0% ⚠︎ | 1.052ms | 2.094ms | 6 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 29.49µs | +35.9% | +35.9% ⚠︎ | 29.17µs | 53.05µs | 6 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 31.09µs | +41.4% | +41.4% ⚠︎ | 31.09µs | 53.68µs | 6 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 41.96µs | +22.0% | +22.0% ⚠︎ | 41.96µs | 70.17µs | 6 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 830.02µs | +28.8% | +28.8% ⚠︎ | 830.02µs | 1.551ms | 6 |

informational; points come from different runners of the same class, so read trends, not single deltas.

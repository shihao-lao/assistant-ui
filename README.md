## aui-perf nightly record

_43 points · 2026-09-03T05:27:14.273Z to 2026-11-21T12:47:01.664Z · latest runner: AMD EPYC 7763 64-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 844.63µs | +34.1% | +34.1% ⚠︎ | 700.12µs | 844.63µs | 2 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 1.233ms | +73.6% | +73.6% ⚠︎ | 1.029ms | 1.233ms | 2 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 53.36µs | +52.8% | +52.8% ⚠︎ | 43.79µs | 53.36µs | 2 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 603.24µs | +56.1% | +56.1% ⚠︎ | 505.83µs | 603.24µs | 2 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 9.296ms | +53.4% | +53.4% ⚠︎ | 7.790ms | 9.296ms | 2 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 264.69µs | +67.7% | +67.7% ⚠︎ | 211.73µs | 264.69µs | 2 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 2.363ms | +64.2% | +64.2% ⚠︎ | 1.933ms | 2.363ms | 2 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 9.243ms | +60.5% | +60.5% ⚠︎ | 7.807ms | 9.243ms | 2 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 9.53µs | +40.9% | +40.9% ⚠︎ | 8.27µs | 9.53µs | 2 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 85.36µs | +55.9% | +55.9% ⚠︎ | 69.58µs | 85.36µs | 2 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 339.32µs | +57.7% | +57.7% ⚠︎ | 273.73µs | 339.32µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 136.51µs |  |  | 80.48µs | 136.51µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 80.22µs |  |  | 43.88µs | 80.22µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 82.46µs |  |  | 43.15µs | 82.46µs | 2 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 310.45µs |  |  | 256.59µs | 310.45µs | 2 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 74.62µs | +111.0% | +111.0% ⚠︎ | 53.43µs | 74.62µs | 2 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 664.05µs | +91.9% | +91.9% ⚠︎ | 516.68µs | 664.05µs | 2 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 9.67µs | +108.8% | +108.8% ⚠︎ | 7.50µs | 9.67µs | 2 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 81.76µs | +111.6% | +111.6% ⚠︎ | 61.86µs | 81.76µs | 2 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 752.62µs | +40.3% | +40.3% ⚠︎ | 596.37µs | 752.62µs | 2 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 5.940ms | +23.7% | +23.7% ⚠︎ | 5.047ms | 5.940ms | 2 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 23.219ms | +21.2% | +21.2% ⚠︎ | 20.030ms | 23.219ms | 2 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 100 parts | 4.009ms |  |  | 2.886ms | 4.009ms | 2 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 2000 parts | 105.431ms |  |  | 91.146ms | 105.431ms | 2 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 500 parts | 17.818ms |  |  | 14.786ms | 17.818ms | 2 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 339.54µs | +2.1% | +2.1% | 285.57µs | 339.54µs | 2 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 3.209ms | +3.8% | +3.8% | 2.785ms | 3.209ms | 2 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 12.690ms | +1.4% | +1.4% | 11.123ms | 12.690ms | 2 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 272.88µs |  |  | 214.74µs | 272.88µs | 2 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.972ms |  |  | 1.401ms | 1.972ms | 2 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 69.37µs | +147.3% | +147.3% ⚠︎ | 50.47µs | 69.37µs | 2 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 696.68µs | +124.0% | +124.0% ⚠︎ | 507.29µs | 696.68µs | 2 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 3.698ms | +122.6% | +122.6% ⚠︎ | 2.689ms | 3.698ms | 2 |
| external-message-conversion › core: external message tool results › 100 matches | 78.74µs | +134.0% | +134.0% ⚠︎ | 59.39µs | 78.74µs | 2 |
| external-message-conversion › core: external message tool results › 1000 matches | 796.72µs | +132.6% | +132.6% ⚠︎ | 600.71µs | 796.72µs | 2 |
| external-message-conversion › core: external message tool results › 5000 matches | 4.162ms | +127.1% | +127.1% ⚠︎ | 3.145ms | 4.162ms | 2 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 43.65µs | +115.2% | +115.2% ⚠︎ | 31.40µs | 43.65µs | 2 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 428.63µs | +115.6% | +115.6% ⚠︎ | 298.11µs | 428.63µs | 2 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 2.255ms | +109.4% | +109.4% ⚠︎ | 1.621ms | 2.255ms | 2 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.27µs | +166.8% | +166.8% ⚠︎ | 0.22µs | 0.27µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.47µs | +130.9% | +130.9% ⚠︎ | 0.36µs | 0.47µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 2.44µs | +102.7% | +102.7% ⚠︎ | 2.15µs | 2.44µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.65µs | +82.5% | +82.5% ⚠︎ | 0.49µs | 0.65µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 3.49µs | +100.7% | +100.7% ⚠︎ | 2.49µs | 3.49µs | 2 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 31.99µs | +105.8% | +105.8% ⚠︎ | 22.78µs | 31.99µs | 2 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 142.82µs | +90.4% | +90.4% ⚠︎ | 113.44µs | 142.82µs | 2 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 801.48µs | +67.2% | +67.2% ⚠︎ | 593.59µs | 801.48µs | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 2.801ms | +143.1% | +143.1% ⚠︎ | 2.109ms | 2.801ms | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 206.84µs | +110.6% | +110.6% ⚠︎ | 161.09µs | 206.84µs | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 3.774ms | +156.1% | +156.1% ⚠︎ | 2.750ms | 3.774ms | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 510.77µs | +135.7% | +135.7% ⚠︎ | 389.52µs | 510.77µs | 2 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 707.61µs | +121.7% | +121.7% ⚠︎ | 505.50µs | 707.61µs | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 7.927ms | +161.6% | +161.6% ⚠︎ | 6.119ms | 7.927ms | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 932.58µs | +100.9% | +100.9% ⚠︎ | 765.77µs | 932.58µs | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 24.635ms | +161.8% | +161.8% ⚠︎ | 16.219ms | 24.635ms | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 3.722ms | +142.7% | +142.7% ⚠︎ | 2.746ms | 3.722ms | 2 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 2.766ms | +143.8% | +143.8% ⚠︎ | 1.933ms | 2.766ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 3.075ms | +193.5% | +193.5% ⚠︎ | 2.321ms | 3.075ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 3.364ms | +133.2% | +133.2% ⚠︎ | 2.482ms | 3.364ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 21.826ms | +192.3% | +192.3% ⚠︎ | 16.672ms | 21.826ms | 2 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 23.291ms | +166.5% | +166.5% ⚠︎ | 17.870ms | 23.291ms | 2 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.483ms | +139.8% | +139.8% ⚠︎ | 1.014ms | 1.483ms | 2 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 3.032ms | +178.3% | +178.3% ⚠︎ | 2.119ms | 3.032ms | 2 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 9.876ms | +127.6% | +127.6% ⚠︎ | 7.448ms | 9.876ms | 2 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.211ms | +7.2% | +7.2% | 1.211ms | 1.295ms | 2 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.959ms | +82.9% | +82.9% ⚠︎ | 1.460ms | 1.959ms | 2 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 5.137ms | +95.8% | +95.8% ⚠︎ | 4.122ms | 5.137ms | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 313.73µs | +159.6% | +159.6% ⚠︎ | 258.66µs | 313.73µs | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 2.582ms | +134.7% | +134.7% ⚠︎ | 2.150ms | 2.582ms | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 291.831ms | +100.7% | +100.7% ⚠︎ | 211.596ms | 291.831ms | 2 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 12.373ms | +128.9% | +128.9% ⚠︎ | 10.712ms | 12.373ms | 2 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 2.22µs | +113.5% | +113.5% ⚠︎ | 1.83µs | 2.22µs | 2 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 9.18µs | +49.9% | +49.9% ⚠︎ | 9.18µs | 9.28µs | 2 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 39.29µs | +72.6% | +72.6% ⚠︎ | 35.94µs | 39.29µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 6.42µs | +142.9% | +142.9% ⚠︎ | 5.57µs | 6.42µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 20.91µs | +78.2% | +78.2% ⚠︎ | 18.44µs | 20.91µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 62.67µs | +147.5% | +147.5% ⚠︎ | 54.67µs | 62.67µs | 2 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 273.80µs | +10.1% | +10.1% ⚠︎ | 245.37µs | 273.80µs | 2 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 6.773ms | +203.9% | +203.9% ⚠︎ | 4.648ms | 6.773ms | 2 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 46.010ms | +202.1% | +202.1% ⚠︎ | 31.278ms | 46.010ms | 2 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 466.148ms | +98.2% | +98.2% ⚠︎ | 389.725ms | 466.148ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 642.57µs | +214.2% | +214.2% ⚠︎ | 445.26µs | 642.57µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 916.28µs | +157.2% | +157.2% ⚠︎ | 698.02µs | 916.28µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 3.625ms | +119.0% | +119.0% ⚠︎ | 3.370ms | 3.625ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 610.83µs | +184.0% | +184.0% ⚠︎ | 450.97µs | 610.83µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.454ms | +130.8% | +130.8% ⚠︎ | 1.130ms | 1.454ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 12.000ms | +120.0% | +120.0% ⚠︎ | 11.112ms | 12.000ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 576.39µs | +198.3% | +198.3% ⚠︎ | 400.82µs | 576.39µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 1.135ms | +205.5% | +205.5% ⚠︎ | 805.82µs | 1.135ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 6.834ms | +106.0% | +106.0% ⚠︎ | 6.834ms | 7.362ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 307.43µs | +222.1% | +222.1% ⚠︎ | 263.16µs | 307.43µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 534.94µs | +165.6% | +165.6% ⚠︎ | 389.75µs | 534.94µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.993ms | +119.6% | +119.6% ⚠︎ | 2.324ms | 2.993ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 23.83µs | +240.8% | +240.8% ⚠︎ | 13.27µs | 23.83µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 39.66µs | +166.7% | +166.7% ⚠︎ | 27.59µs | 39.66µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 262.48µs | +145.9% | +145.9% ⚠︎ | 205.05µs | 262.48µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 658.98µs | +260.0% | +260.0% ⚠︎ | 450.76µs | 658.98µs | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 1.098ms | +183.7% | +183.7% ⚠︎ | 812.00µs | 1.098ms | 2 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 7.121ms | +149.1% | +149.1% ⚠︎ | 6.341ms | 7.121ms | 2 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 250.45µs | +78.5% | +78.5% ⚠︎ | 198.90µs | 250.45µs | 2 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 2.151ms | +69.4% | +69.4% ⚠︎ | 1.767ms | 2.151ms | 2 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 1.081ms | +66.4% | +66.4% ⚠︎ | 884.10µs | 1.081ms | 2 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 307.87µs | +30.3% | +30.3% ⚠︎ | 242.54µs | 307.87µs | 2 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 2.535ms | +23.2% | +23.2% ⚠︎ | 2.140ms | 2.535ms | 2 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 1.290ms | +23.6% | +23.6% ⚠︎ | 1.078ms | 1.290ms | 2 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 350.32µs | +144.1% | +144.1% ⚠︎ | 266.94µs | 350.32µs | 2 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 25.881ms | +94.2% | +94.2% ⚠︎ | 20.581ms | 25.881ms | 2 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 668.294ms | +104.3% | +104.3% ⚠︎ | 472.059ms | 668.294ms | 2 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 233.93µs | +10.8% | +10.8% ⚠︎ | 187.75µs | 233.93µs | 2 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.827ms | +3.2% | +3.2% | 1.552ms | 1.827ms | 2 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 936.55µs | +4.6% | +4.6% | 793.67µs | 936.55µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 208.09µs |  |  | 162.92µs | 208.09µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 939.43µs |  |  | 740.00µs | 939.43µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 229.60µs |  |  | 177.32µs | 229.60µs | 2 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 1.013ms |  |  | 789.57µs | 1.013ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 3.543ms | +136.8% | +136.8% ⚠︎ | 2.675ms | 3.543ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 3.540ms | +137.4% | +137.4% ⚠︎ | 2.729ms | 3.540ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 3.499ms | +144.1% | +144.1% ⚠︎ | 2.642ms | 3.499ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 3.670ms | +155.4% | +155.4% ⚠︎ | 2.693ms | 3.670ms | 2 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 2.204ms | +148.2% | +148.2% ⚠︎ | 1.750ms | 2.204ms | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 3.353ms | +138.7% | +138.7% ⚠︎ | 2.539ms | 3.353ms | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 3.339ms | +144.5% | +144.5% ⚠︎ | 2.550ms | 3.339ms | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 235.74µs | +89.4% | +89.4% ⚠︎ | 199.59µs | 235.74µs | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 145.22µs | +133.0% | +133.0% ⚠︎ | 106.93µs | 145.22µs | 2 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.723ms | +139.3% | +139.3% ⚠︎ | 1.339ms | 1.723ms | 2 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.976ms | +166.5% | +166.5% ⚠︎ | 1.423ms | 1.976ms | 2 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 2.094ms | +178.6% | +178.6% ⚠︎ | 1.509ms | 2.094ms | 2 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 53.05µs | +144.4% | +144.4% ⚠︎ | 37.94µs | 53.05µs | 2 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 53.68µs | +144.3% | +144.3% ⚠︎ | 40.39µs | 53.68µs | 2 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 70.17µs | +104.1% | +104.1% ⚠︎ | 53.66µs | 70.17µs | 2 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 1.551ms | +140.6% | +140.6% ⚠︎ | 1.127ms | 1.551ms | 2 |

informational; points come from different runners of the same class, so read trends, not single deltas.

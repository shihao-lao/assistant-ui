## aui-perf nightly record

_42 points · 2026-09-03T05:27:14.273Z to 2026-11-20T13:01:26.923Z · latest runner: AMD EPYC 9V74 80-Core Processor · Node v26.13.0_

| bench | latest | Δ7d | Δ30d | min | max | points |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 chunks from one source stream | 700.12µs | +11.1% | +11.1% ⚠︎ | 700.12µs | 700.12µs | 1 |
| accumulator › assistant-stream: raw controller enqueue overhead › 10,000 controller.enqueue calls | 1.029ms | +44.9% | +44.9% ⚠︎ | 1.029ms | 1.029ms | 1 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 16 deltas × 250 chars | 43.79µs | +25.4% | +25.4% ⚠︎ | 43.79µs | 43.79µs | 1 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 250 deltas × 16 chars | 505.83µs | +30.9% | +30.9% ⚠︎ | 505.83µs | 505.83µs | 1 |
| accumulator › assistant-stream: same 4000-char text, chunk size A/B › 4000 deltas × 1 char (per-token) | 7.790ms | +28.6% | +28.6% ⚠︎ | 7.790ms | 7.790ms | 1 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 100 deltas | 211.73µs | +34.2% | +34.2% ⚠︎ | 211.73µs | 211.73µs | 1 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 1000 deltas | 1.933ms | +34.3% | +34.3% ⚠︎ | 1.933ms | 1.933ms | 1 |
| accumulator › assistant-stream: stream + accumulator per-delta cost (16-char deltas) › 4000 deltas | 7.807ms | +35.6% | +35.6% ⚠︎ | 7.807ms | 7.807ms | 1 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 100 deltas | 8.27µs | +22.2% | +22.2% ⚠︎ | 8.27µs | 8.27µs | 1 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 1000 deltas | 69.58µs | +27.1% | +27.1% ⚠︎ | 69.58µs | 69.58µs | 1 |
| accumulator › assistant-stream: stream round trip baseline, no accumulator › 4000 deltas | 273.73µs | +27.2% | +27.2% ⚠︎ | 273.73µs | 273.73µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 128 parts, distinct providers (stress) | 80.48µs |  |  | 80.48µs | 80.48µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 16 parts, one repeated provider | 43.88µs |  |  | 43.88µs | 43.88µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 2 parts, one repeated provider | 43.15µs |  |  | 43.15µs | 43.15µs | 1 |
| ai-sdk-system-metadata › ai-sdk: system-message metadata conversion through the runtime › 512 parts, distinct providers (stress) | 256.59µs |  |  | 256.59µs | 256.59µs | 1 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 10 static tools | 53.43µs | +51.1% | +51.1% ⚠︎ | 53.43µs | 53.43µs | 1 |
| ai-sdk-toolkit › ai-sdk: convert fresh AISDKToolkit schemas › 100 static tools | 516.68µs | +49.3% | +49.3% ⚠︎ | 516.68µs | 516.68µs | 1 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 10 static tools | 7.50µs | +62.0% | +62.0% ⚠︎ | 7.50µs | 7.50µs | 1 |
| ai-sdk-toolkit › ai-sdk: reuse converted AISDKToolkit schemas › 100 static tools | 61.86µs | +60.1% | +60.1% ⚠︎ | 61.86µs | 61.86µs | 1 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 100 deltas | 596.37µs | +11.1% | +11.1% ⚠︎ | 596.37µs | 596.37µs | 1 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 1000 deltas | 5.047ms | +5.1% | +5.1% | 5.047ms | 5.047ms | 1 |
| data-stream › assistant-stream: data stream decode (16-char deltas) › 4000 deltas | 20.030ms | +4.5% | +4.5% | 20.030ms | 20.030ms | 1 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 100 parts | 2.886ms |  |  | 2.886ms | 2.886ms | 1 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 2000 parts | 91.146ms |  |  | 91.146ms | 91.146ms | 1 |
| data-stream › assistant-stream: data stream decode + accumulate, one tool-call start per part › 500 parts | 14.786ms |  |  | 14.786ms | 14.786ms | 1 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 100 deltas | 285.57µs | -14.1% | -14.1% ⚠︎ | 285.57µs | 285.57µs | 1 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 1000 deltas | 2.785ms | -9.9% | -9.9% | 2.785ms | 2.785ms | 1 |
| data-stream › assistant-stream: data stream encode (16-char deltas) › 4000 deltas | 11.123ms | -11.1% | -11.1% ⚠︎ | 11.123ms | 11.123ms | 1 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 1000 messages, 6-part replies | 214.74µs |  |  | 214.74µs | 214.74µs | 1 |
| external-message-conversion › core: cached external message conversion, one streaming delta › 5000 messages, 20-part replies | 1.401ms |  |  | 1.401ms | 1.401ms | 1 |
| external-message-conversion › core: external message reasoning continuations › 100 matches | 50.47µs | +79.9% | +79.9% ⚠︎ | 50.47µs | 50.47µs | 1 |
| external-message-conversion › core: external message reasoning continuations › 1000 matches | 507.29µs | +63.1% | +63.1% ⚠︎ | 507.29µs | 507.29µs | 1 |
| external-message-conversion › core: external message reasoning continuations › 5000 matches | 2.689ms | +61.9% | +61.9% ⚠︎ | 2.689ms | 2.689ms | 1 |
| external-message-conversion › core: external message tool results › 100 matches | 59.39µs | +76.5% | +76.5% ⚠︎ | 59.39µs | 59.39µs | 1 |
| external-message-conversion › core: external message tool results › 1000 matches | 600.71µs | +75.4% | +75.4% ⚠︎ | 600.71µs | 600.71µs | 1 |
| external-message-conversion › core: external message tool results › 5000 matches | 3.145ms | +71.6% | +71.6% ⚠︎ | 3.145ms | 3.145ms | 1 |
| external-message-conversion › core: external message unique tool calls › 100 matches | 31.40µs | +54.8% | +54.8% ⚠︎ | 31.40µs | 31.40µs | 1 |
| external-message-conversion › core: external message unique tool calls › 1000 matches | 298.11µs | +50.0% | +50.0% ⚠︎ | 298.11µs | 298.11µs | 1 |
| external-message-conversion › core: external message unique tool calls › 5000 matches | 1.621ms | +50.6% | +50.6% ⚠︎ | 1.621ms | 1.621ms | 1 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 1 text parts | 0.22µs | +109.4% | +109.4% ⚠︎ | 0.22µs | 0.22µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 10 text parts | 0.36µs | +79.2% | +79.2% ⚠︎ | 0.36µs | 0.36µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike text parts › 100 text parts | 2.15µs | +78.3% | +78.3% ⚠︎ | 2.15µs | 2.15µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 1 tool calls | 0.49µs | +36.7% | +36.7% ⚠︎ | 0.49µs | 0.49µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 10 tool calls | 2.49µs | +43.1% | +43.1% ⚠︎ | 2.49µs | 2.49µs | 1 |
| from-thread-message-like › core: fromThreadMessageLike tool calls › 100 tool calls | 22.78µs | +46.6% | +46.6% ⚠︎ | 22.78µs | 22.78µs | 1 |
| interactable-array-patches › core: id-keyed interactable array patches › 1000 items and patches | 113.44µs | +51.3% | +51.3% ⚠︎ | 113.44µs | 113.44µs | 1 |
| interactable-array-patches › core: id-keyed interactable array patches › 5000 items and patches | 593.59µs | +23.8% | +23.8% ⚠︎ | 593.59µs | 593.59µs | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tilde runs on one line | 2.109ms | +83.0% | +83.0% ⚠︎ | 2.109ms | 2.109ms | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 tildes after prose | 161.09µs | +64.0% | +64.0% ⚠︎ | 161.09µs | 161.09µs | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 20,000 triple-backtick spans on one line | 2.750ms | +86.7% | +86.7% ⚠︎ | 2.750ms | 2.750ms | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, 5,000 code spans in one paragraph | 389.52µs | +79.7% | +79.7% ⚠︎ | 389.52µs | 389.52µs | 1 |
| markdown-preprocess › react-markdown: preprocess › escapeCurrencyDollars, mixed message, 100 sections | 505.50µs | +58.4% | +58.4% ⚠︎ | 505.50µs | 505.50µs | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tilde runs on one line | 6.119ms | +102.0% | +102.0% ⚠︎ | 6.119ms | 6.119ms | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 tildes after prose | 765.77µs | +65.0% | +65.0% ⚠︎ | 765.77µs | 765.77µs | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 20,000 triple-backtick spans on one line | 16.219ms | +72.4% | +72.4% ⚠︎ | 16.219ms | 16.219ms | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, 5,000 code spans in one paragraph | 2.746ms | +79.0% | +79.0% ⚠︎ | 2.746ms | 2.746ms | 1 |
| markdown-preprocess › react-markdown: preprocess › normalizeMathDelimiters, mixed message, 100 sections | 1.933ms | +70.4% | +70.4% ⚠︎ | 1.933ms | 1.933ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown | 2.321ms | +121.5% | +121.5% ⚠︎ | 2.321ms | 2.321ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 10 KB fenced Markdown deferred | 2.482ms | +72.0% | +72.0% ⚠︎ | 2.482ms | 2.482ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown | 16.672ms | +123.3% | +123.3% ⚠︎ | 16.672ms | 16.672ms | 1 |
| markdown-streaming › react-markdown: one token after an unchanged fenced code block › 100 KB fenced Markdown deferred | 17.870ms | +104.4% | +104.4% ⚠︎ | 17.870ms | 17.870ms | 1 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 1 paragraphs | 1.014ms | +64.0% | +64.0% ⚠︎ | 1.014ms | 1.014ms | 1 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 10 paragraphs | 2.119ms | +94.5% | +94.5% ⚠︎ | 2.119ms | 2.119ms | 1 |
| markdown-streaming › react-markdown: one token changed in the last paragraph, by message length › 50 paragraphs | 7.448ms | +71.7% | +71.7% ⚠︎ | 7.448ms | 7.448ms | 1 |
| markdown-streaming › react-markdown: the same token with defer on › 1 paragraphs deferred | 1.295ms | +14.7% | +14.7% ⚠︎ | 1.295ms | 1.295ms | 1 |
| markdown-streaming › react-markdown: the same token with defer on › 10 paragraphs deferred | 1.460ms | +36.3% | +36.3% ⚠︎ | 1.460ms | 1.460ms | 1 |
| markdown-streaming › react-markdown: the same token with defer on › 50 paragraphs deferred | 4.122ms | +57.1% | +57.1% ⚠︎ | 4.122ms | 4.122ms | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 1000 character argument in 16-character deltas | 258.66µs | +114.0% | +114.0% ⚠︎ | 258.66µs | 258.66µs | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 10000 character argument in 16-character deltas | 2.150ms | +95.5% | +95.5% ⚠︎ | 2.150ms | 2.150ms | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 500 short object entries in 16-character deltas | 211.596ms | +45.5% | +45.5% ⚠︎ | 211.596ms | 211.596ms | 1 |
| react-langgraph › react-langgraph: streamed tool argument accumulation › 50000 character argument in 16-character deltas | 10.712ms | +98.2% | +98.2% ⚠︎ | 10.712ms | 10.712ms | 1 |
| react-pi-message-projection › react-pi: streaming tail projection › 10 stable messages | 1.83µs | +76.5% | +76.5% ⚠︎ | 1.83µs | 1.83µs | 1 |
| react-pi-message-projection › react-pi: streaming tail projection › 1000 stable messages | 9.28µs | +51.5% | +51.5% ⚠︎ | 9.28µs | 9.28µs | 1 |
| react-pi-message-projection › react-pi: streaming tail projection › 5000 stable messages | 35.94µs | +57.9% | +57.9% ⚠︎ | 35.94µs | 35.94µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 1 chunks | 5.57µs | +110.8% | +110.8% ⚠︎ | 5.57µs | 5.57µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 100 KiB, 101 chunks | 18.44µs | +57.1% | +57.1% ⚠︎ | 18.44µs | 18.44µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1 chunks | 54.67µs | +115.9% | +115.9% ⚠︎ | 54.67µs | 54.67µs | 1 |
| sse-fragmentation › assistant-stream: fragmented SSE events › 1024 KiB, 1025 chunks | 245.37µs | -1.4% | -1.4% | 245.37µs | 245.37µs | 1 |
| thread-scaling › external-store thread: mount+unmount by message count › 10 messages | 4.648ms | +108.6% | +108.6% ⚠︎ | 4.648ms | 4.648ms | 1 |
| thread-scaling › external-store thread: mount+unmount by message count › 100 messages | 31.278ms | +105.4% | +105.4% ⚠︎ | 31.278ms | 31.278ms | 1 |
| thread-scaling › external-store thread: mount+unmount by message count › 1000 messages | 389.725ms | +65.7% | +65.7% ⚠︎ | 389.725ms | 389.725ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 10 messages | 445.26µs | +117.7% | +117.7% ⚠︎ | 445.26µs | 445.26µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 100 messages | 698.02µs | +96.0% | +96.0% ⚠︎ | 698.02µs | 698.02µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › 20 message window, 1000 messages | 3.370ms | +103.6% | +103.6% ⚠︎ | 3.370ms | 3.370ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 10 messages | 450.97µs | +109.7% | +109.7% ⚠︎ | 450.97µs | 450.97µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 100 messages | 1.130ms | +79.3% | +79.3% ⚠︎ | 1.130ms | 1.130ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages by id, 1000 messages | 11.112ms | +103.8% | +103.8% ⚠︎ | 11.112ms | 11.112ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 10 messages | 400.82µs | +107.5% | +107.5% ⚠︎ | 400.82µs | 400.82µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 100 messages | 805.82µs | +116.9% | +116.9% ⚠︎ | 805.82µs | 805.82µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › all messages, 1000 messages | 7.362ms | +121.9% | +121.9% ⚠︎ | 7.362ms | 7.362ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 10 messages | 263.16µs | +175.7% | +175.7% ⚠︎ | 263.16µs | 263.16µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 100 messages | 389.75µs | +93.5% | +93.5% ⚠︎ | 389.75µs | 389.75µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › provider only, 1000 messages | 2.324ms | +70.5% | +70.5% ⚠︎ | 2.324ms | 2.324ms | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 10 messages | 13.27µs | +89.8% | +89.8% ⚠︎ | 13.27µs | 13.27µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 100 messages | 27.59µs | +85.6% | +85.6% ⚠︎ | 27.59µs | 27.59µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by layer › runtime only, 1000 messages | 205.05µs | +92.1% | +92.1% ⚠︎ | 205.05µs | 205.05µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 10 messages | 450.76µs | +146.2% | +146.2% ⚠︎ | 450.76µs | 450.76µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 100 messages | 812.00µs | +109.7% | +109.7% ⚠︎ | 812.00µs | 812.00µs | 1 |
| thread-scaling › external-store thread: one token changed in the last message, by thread length › 1000 messages | 6.341ms | +121.8% | +121.8% ⚠︎ | 6.341ms | 6.341ms | 1 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 1000 bytes | 198.90µs | +41.7% | +41.7% ⚠︎ | 198.90µs | 198.90µs | 1 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 10000 bytes | 1.767ms | +39.1% | +39.1% ⚠︎ | 1.767ms | 1.767ms | 1 |
| tool-args › assistant-stream: accumulator tool arguments (16-char deltas) › 5000 bytes | 884.10µs | +36.1% | +36.1% ⚠︎ | 884.10µs | 884.10µs | 1 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 1000 bytes | 242.54µs | +2.7% | +2.7% | 242.54µs | 242.54µs | 1 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 10000 bytes | 2.140ms | +4.0% | +4.0% | 2.140ms | 2.140ms | 1 |
| tool-args › assistant-stream: active-reader tool arguments (16-char deltas) › 5000 bytes | 1.078ms | +3.3% | +3.3% | 1.078ms | 1.078ms | 1 |
| tool-args › assistant-stream: complete accumulated arguments (single delta) › 10,000 array elements | 266.94µs | +86.0% | +86.0% ⚠︎ | 266.94µs | 266.94µs | 1 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 array entries | 20.581ms | +54.4% | +54.4% ⚠︎ | 20.581ms | 20.581ms | 1 |
| tool-args › assistant-stream: dense accumulated arguments (16-char deltas) › 2,000 object entries | 472.059ms | +44.3% | +44.3% ⚠︎ | 472.059ms | 472.059ms | 1 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 1000 bytes | 187.75µs | -11.1% | -11.1% ⚠︎ | 187.75µs | 187.75µs | 1 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 10000 bytes | 1.552ms | -12.3% | -12.3% ⚠︎ | 1.552ms | 1.552ms | 1 |
| tool-args › assistant-stream: execute-only tool arguments (16-char deltas) › 5000 bytes | 793.67µs | -11.3% | -11.3% ⚠︎ | 793.67µs | 793.67µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 10000 bytes | 162.92µs |  |  | 162.92µs | 162.92µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › accumulator: 50000 bytes | 740.00µs |  |  | 740.00µs | 740.00µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 10000 bytes | 177.32µs |  |  | 177.32µs | 177.32µs | 1 |
| tool-args › assistant-stream: long string arguments (4096-char deltas) › active-reader: 50000 bytes | 789.57µs |  |  | 789.57µs | 789.57µs | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRoot | 2.675ms | +78.8% | +78.8% ⚠︎ | 2.675ms | 2.675ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootDeps | 2.729ms | +83.1% | +83.1% ⚠︎ | 2.729ms | 2.729ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › createTapRootStable | 2.642ms | +84.3% | +84.3% ⚠︎ | 2.642ms | 2.642ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › react | 2.693ms | +87.4% | +87.4% ⚠︎ | 2.693ms | 2.693ms | 1 |
| tree › tree mount+unmount, 500 leaves x 10 hooks › tapRoot | 1.750ms | +97.0% | +97.0% ⚠︎ | 1.750ms | 1.750ms | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRoot | 2.539ms | +80.7% | +80.7% ⚠︎ | 2.539ms | 2.539ms | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootDeps | 2.550ms | +86.7% | +86.7% ⚠︎ | 2.550ms | 2.550ms | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › createTapRootStable | 199.59µs | +60.4% | +60.4% ⚠︎ | 199.59µs | 199.59µs | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › react | 106.93µs | +71.6% | +71.6% ⚠︎ | 106.93µs | 106.93µs | 1 |
| tree › tree update: one leaf dispatch, 500 leaves x 10 hooks › tapRoot | 1.339ms | +86.0% | +86.0% ⚠︎ | 1.339ms | 1.339ms | 1 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › deps | 1.423ms | +91.9% | +91.9% ⚠︎ | 1.423ms | 1.423ms | 1 |
| useResources › useResources mount+unmount, 500 children x 10 hooks › no-deps | 1.509ms | +100.7% | +100.7% ⚠︎ | 1.509ms | 1.509ms | 1 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › deps | 37.94µs | +74.8% | +74.8% ⚠︎ | 37.94µs | 37.94µs | 1 |
| useResources › useResources: one child dispatch, 500 children x 10 hooks › no-deps | 40.39µs | +83.8% | +83.8% ⚠︎ | 40.39µs | 40.39µs | 1 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › deps | 53.66µs | +56.1% | +56.1% ⚠︎ | 53.66µs | 53.66µs | 1 |
| useResources › useResources: rebuild elements array, 500 children x 10 hooks › no-deps | 1.127ms | +74.9% | +74.9% ⚠︎ | 1.127ms | 1.127ms | 1 |

informational; points come from different runners of the same class, so read trends, not single deltas.

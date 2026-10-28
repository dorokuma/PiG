### Fixed

- The Durable core conformance gate no longer writes the reference checkout from a vitest run: its cache lives in the run's output directory. The default, `packages/durable/node_modules/.vite`, added `node_modules` to the listing E17 and E18 print with `ls`, which they capture once for the reference before any U row ran, so `make durable-contract` failed both rows against every build on a fresh clone. <!-- fix: dd473e5ab4df7097e5018bdeb007d647551967d9 -->

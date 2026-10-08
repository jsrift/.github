# jsrift

jsrift takes obfuscated JavaScript and gives back code a person can read. It
undoes the layers that tools such as obfuscator.io add: encoded string tables,
flattened control flow, proxy functions, dead code, anti-debugging guards and
mangled names.

It only changes what it can show to be equivalent. When a rewrite cannot be
verified, the code is left as it was and the report says why.

## Where things live

- **[jsrift.github.io](https://jsrift.github.io)**: the web app. Paste code or
  drop a file, pick a preset, press Run. Everything runs in your browser;
  nothing is uploaded.
- **[jsrift](https://github.com/jsrift/jsrift)**: the engine, published on npm
  as `@jsrift/core`, for use from Node or in a Web Worker.
- **[cli](https://github.com/jsrift/cli)**: the `jsrift` command, published on
  npm as `@jsrift/cli`.

## Presets

- **conservative** applies only rewrites that are provably identical.
- **balanced** adds the assumptions that hold for mainstream obfuscators and
  says so in the report. This is the default.
- **aggressive** goes further for readability and discloses every step that
  may differ.

All of it is MIT licensed. Issues and pull requests go to the repository they
concern.

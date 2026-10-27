# dsh-preview-evidence

Before/after screenshots backing a community bug discussion on `deepseek-ai/deepseek-harness`:
on HarmonyOS ArkWeb (and other non-WHATWG-conforming engines) every DSH Web file preview fails with 「文件资源服务不可用」 because `protocolOf()` relies on `new URL().hostname`.

- `before_html.jpg` — preview panel shows the error (original bundle)
- `after_html.jpg` — same session, same file, renders correctly (locally patched bundle)

The patch is a **local, community-verified** change to the shipped bundle; it is not an official fix.

---
license: apache-2.0
pipeline_tag: text-generation
frameworks:
 - pt
 - ms
---

---
license: apache-2.0
pipeline_tag: text-generation
frameworks:
 - pt
 - ms
---

export const getYamlHeader = (md: string) => {
  const match = /---([\s\S]+?)---/.exec(md);
  return match ? match[1] : '';
};

export const getYamlFrontMatter = (markdown: string) => {
  const regex = /^---\r?\n([\s\S]*?)\r?\n---\r?\n/;
  const match = markdown.match(regex);
  return match ? match[1] : '';
};

## Hi there 👋

<!--
**adityaaryan0003/adityaaryan0003** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
import { generateSnakeAnimation } from "generate-snake-animation";

const outputs = [
  {
    format: "svg",
    drawOptions: {
      // ..
    },
  },
];

const results = await generateSnakeAnimation(
  {
    platform: "github", // supports github, gitlab and forgejo (codeberg)
    username: "platane",
    githubToken: process.env.GITHUB_TOKEN,
  },
  outputs,
);

fs.writeFileSync("snake.svg", results[0]);

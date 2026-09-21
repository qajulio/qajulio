## JULIO MISHIMA - QA AI-1st (CTFL-AT)

Quality Assurance focused on test automation, quality test, and AI-driven solutions.


<p align="center">
  <a href="https://github.com/qajulio">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/jhmjulio/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
</p>


### #️⃣ Focus

Automation · Quality Test · AI · CI/CD - GitHubActions
Projects
AI QA DIY
QA Automation


### #️⃣ Stack

VSCode · Playwright · Cypress · JavaScript · GitHub Actions


<meta charset="UTF-8">
  <title>Meus projetos GitHub</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 900px;
      margin: 40px auto;
      padding: 20px;
    }

    .repositorio {
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 20px;
      margin-bottom: 15px;
    }

    .repositorio h2 {
      margin-top: 0;
    }

    .repositorio a {
      color: #0969da;
      text-decoration: none;
    }
  </style>
</head>

<body>

  <h1>🚀 Meus projetos</h1>

  <div id="repositorios">
    Carregando...
  </div>

  <script>
    const usuario = "qajulio";

    fetch(`https://api.github.com/users/${usuario}/repos?sort=updated&per_page=10`)
      .then(response => response.json())
      .then(repositorios => {

        const container = document.getElementById("repositorios");

        container.innerHTML = "";

        repositorios
          .filter(repo => !repo.fork)
          .forEach(repo => {

            const div = document.createElement("div");

            div.className = "repositorio";

            div.innerHTML = `
              <h2>
                <a href="${repo.html_url}" target="_blank">
                  ${repo.name}
                </a>
              </h2>

              <p>
                ${repo.description || "Sem descrição"}
              </p>

              <p>
                ⭐ ${repo.stargazers_count}
                &nbsp;&nbsp;
                🍴 ${repo.forks_count}
                &nbsp;&nbsp;
                💻 ${repo.language || "Não informado"}
              </p>
            `;

            container.appendChild(div);
          });
      })
      .catch(error => {
        document.getElementById("repositorios").innerHTML =
          "Erro ao carregar os repositórios.";
      });
  </script>

</body>

(By Julio Mishima - CTAI.)

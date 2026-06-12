# 💫 About Me:youtube-ai-agent/
│
├── .github/workflows/youtube.yml
├── agent.py
├── config.py
├── output/
│   └── result.txt
└── README.mdname: Full YouTube AI Agent

on:
  schedule:
    - cron: "0 8 * * *"
  workflow_dispatch:

jobs:
  run-agent:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Setup Python
        uses: actions/setup-python@v4
        with:
          python-version: "3.10"

      - name: Install dependencies
        run: pip install openai requests

      - name: Run AI Agent
        env:
          OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}
        run: python agent.pyimport openai
import os

openai.api_key = os.getenv("OPENAI_API_KEY")

prompt = """
You are a professional YouTube growth AI expert.

Generate:

1. Viral video idea (Emotional / Love / Motivation / Story)
2. Full short video script (60 seconds, Hindi + English mix)
3. Catchy viral title (clickbait style)
4. SEO description
5. 10 trending hashtags
6. Thumbnail idea (text + visual description)
7. Upload timing suggestion

Make it highly viral and emotional.
"""

response = openai.ChatCompletion.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": prompt}]
)

result = response["choices"][0]["message"]["content"]

os.makedirs("output", exist_ok=True)

with open("output/result.txt", "w", encoding="utf-8") as f:
    f.write(result)

print("YouTube AI content generated successfully!")
Welcome to my YouTube channel 
🔥 Title:
Gareeb Ladka vs Rich Girl Emotional Story 💔

🎬 Script:
Ek chhota sa gaon tha jahan ek ladka...

📝 Description:
Ye story aapke dil ko tod degi aur jod bhi degi...

#Hashtags:
#emotional #love #story #hindistory #viral

🖼 Thumbnail Idea:
Boy crying in rain, rich girl walking away, dramatic lighting

⏰ Best Upload Time:
7:00 PM IST (High engagement)

## 🌐 Socials:
[![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/@https://www.youtube.com/@FilmRevelationX1.50) 

# 💻 Tech Stack:
![PlayStation Network](https://img.shields.io/badge/PSN-%230070D1.svg?style=for-the-badge&logo=Playstation&logoColor=white) ![Itch.io](https://img.shields.io/badge/Itch-%23FF0B34.svg?style=for-the-badge&logo=Itch.io&logoColor=white) ![Unreal Engine](https://img.shields.io/badge/unrealengine-%23313131.svg?style=for-the-badge&logo=unrealengine&logoColor=white) ![Xbox](https://img.shields.io/badge/xbox-%23107C10.svg?style=for-the-badge&logo=xbox&logoColor=white) ![Epic Games](https://img.shields.io/badge/epicgames-%23313131.svg?style=for-the-badge&logo=epicgames&logoColor=white) ![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white) ![Tampermonkey](https://img.shields.io/badge/tampermonkey-%2300485B.svg?style=for-the-badge&logo=tampermonkey&logoColor=white) ![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white) ![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![Home Assistant](https://img.shields.io/badge/home%20assistant-%2341BDF5.svg?style=for-the-badge&logo=home-assistant&logoColor=white) ![ElasticSearch](https://img.shields.io/badge/-ElasticSearch-005571?style=for-the-badge&logo=elasticsearch) ![Crowdin](https://img.shields.io/badge/Crowdin-2E3340.svg?style=for-the-badge&logo=Crowdin&logoColor=white) ![Babel](https://img.shields.io/badge/Babel-F9DC3e?style=for-the-badge&logo=babel&logoColor=black) ![Bitwarden](https://img.shields.io/badge/bitwarden-%23175DDC.svg?style=for-the-badge&logo=bitwarden&logoColor=white) ![Alfred](https://img.shields.io/badge/alfred-%235C1F87.svg?style=for-the-badge&logo=alfred) ![Ansible](https://img.shields.io/badge/ansible-%231A1918.svg?style=for-the-badge&logo=ansible&logoColor=white) ![Airbnb](https://img.shields.io/badge/Airbnb-%23ff5a5f.svg?style=for-the-badge&logo=Airbnb&logoColor=white) ![Vitest](https://img.shields.io/badge/-Vitest-252529?style=for-the-badge&logo=vitest&logoColor=FCC72B) ![Puppeteer](https://img.shields.io/badge/Puppeteer-%2340B5A4.svg?style=for-the-badge&logo=Puppeteer&logoSize=auto&logoColor=black) ![Cypress](https://img.shields.io/badge/-cypress-%23E5E5E5?style=for-the-badge&logo=cypress&logoColor=058a5e) ![Playwright](https://img.shields.io/badge/-playwright-%232EAD33?style=for-the-badge&logo=playwright&logoColor=white) ![Testing-Library](https://img.shields.io/badge/-TestingLibrary-%23E33332?style=for-the-badge&logo=testing-library&logoColor=white) ![Jest](https://img.shields.io/badge/-jest-%23C21325?style=for-the-badge&logo=jest&logoColor=white) ![Octopus Deploy](https://img.shields.io/badge/octopus%20deploy-0D80D8?style=for-the-badge&logo=octopusdeploy&logoColor=white) ![CircleCI](https://img.shields.io/badge/circleci-%23161616.svg?style=for-the-badge&logo=circleci&logoColor=white) ![ChipperCI](https://img.shields.io/badge/chipperci-1e394e.svg?style=for-the-badge&logo=chipperci&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![GitLab CI](https://img.shields.io/badge/gitlab%20CI-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white) ![Gitee](https://img.shields.io/badge/Gitee-C71D23?style=for-the-badge&logo=gitee&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white) ![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white) ![Bitbucket](https://img.shields.io/badge/bitbucket-%230047B3.svg?style=for-the-badge&logo=bitbucket&logoColor=white) ![Gitpod](https://img.shields.io/badge/gitpod-f06611.svg?style=for-the-badge&logo=gitpod&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white) ![Scipy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![Dribbble](https://img.shields.io/badge/Dribbble-EA4C89?style=for-the-badge&logo=dribbble&logoColor=white) ![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) ![Krita](https://img.shields.io/badge/Krita-203759?style=for-the-badge&logo=krita&logoColor=EEF37B) ![Proto.io](https://img.shields.io/badge/Proto.io-161637?style=for-the-badge&logo=proto.io&logoColor=00e5ff) ![Sketch Up](https://img.shields.io/badge/SketchUp-005F9E?style=for-the-badge&logo=sketchup&logoColor=white) ![Storybook](https://img.shields.io/badge/-Storybook-FF4785?style=for-the-badge&logo=storybook&logoColor=white) ![Adobe XD](https://img.shields.io/badge/Adobe%20XD-470137?style=for-the-badge&logo=Adobe%20XD&logoColor=#FF61F6) ![Affinity Designer](https://img.shields.io/badge/affinity%20desginer-%231B72BE.svg?style=for-the-badge&logo=affinity-designer&logoColor=white) ![Blender](https://img.shields.io/badge/blender-%23F5792A.svg?style=for-the-badge&logo=blender&logoColor=white) ![Affinity Photo](https://img.shields.io/badge/affinityphoto-%237E4DD2.svg?style=for-the-badge&logo=affinity-photo&logoColor=white) ![Adobe Photoshop](https://img.shields.io/badge/adobe%20photoshop-%2331A8FF.svg?style=for-the-badge&logo=adobe%20photoshop&logoColor=white) ![Adobe Premiere Pro](https://img.shields.io/badge/Adobe%20Premiere%20Pro-9999FF.svg?style=for-the-badge&logo=Adobe%20Premiere%20Pro&logoColor=white) ![Adobe Lightroom Classic](https://img.shields.io/badge/Adobe%20Lightroom%20Classic-31A8FF.svg?style=for-the-badge&logo=Adobe%20Lightroom%20Classic&logoColor=white) ![Adobe InDesign](https://img.shields.io/badge/Adobe%20InDesign-49021F?style=for-the-badge&logo=adobeindesign&logoColor=FF3366) ![Adobe Audition](https://img.shields.io/badge/Adobe%20Audition-9999FF.svg?style=for-the-badge&logo=Adobe%20Audition&logoColor=white) ![Adobe Dreamweaver](https://img.shields.io/badge/Adobe%20Dreamweaver-FF61F6.svg?style=for-the-badge&logo=Adobe%20Dreamweaver&logoColor=white) ![Adobe Fonts](https://img.shields.io/badge/Adobe%20Fonts-000B1D.svg?style=for-the-badge&logo=Adobe%20Fonts&logoColor=white) ![Adobe Illustrator](https://img.shields.io/badge/adobe%20illustrator-%23FF9A00.svg?style=for-the-badge&logo=adobe%20illustrator&logoColor=white) ![Adobe Acrobat Reader](https://img.shields.io/badge/Adobe%20Acrobat%20Reader-EC1C24.svg?style=for-the-badge&logo=Adobe%20Acrobat%20Reader&logoColor=white) ![Adobe After Effects](https://img.shields.io/badge/Adobe%20After%20Effects-9999FF.svg?style=for-the-badge&logo=Adobe%20After%20Effects&logoColor=white) ![Adobe](https://img.shields.io/badge/adobe-%23FF0000.svg?style=for-the-badge&logo=adobe&logoColor=white) ![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white) ![Single Store](https://img.shields.io/badge/Single%20Store-AA00FF?style=for-the-badge&logo=singlestore&logoColor=white) ![PlanetScale](https://img.shields.io/badge/planetscale-%23000000.svg?style=for-the-badge&logo=planetscale&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![MusicBrainz](https://img.shields.io/badge/Musicbrainz-EB743B?style=for-the-badge&logo=musicbrainz&logoColor=BA478F) ![MicrosoftSQLServer](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white) ![Firebase](https://img.shields.io/badge/firebase-a08021?style=for-the-badge&logo=firebase&logoColor=ffcd34) ![CockroachLabs](https://img.shields.io/badge/Cockroach%20Labs-6933FF?style=for-the-badge&logo=Cockroach%20Labs&logoColor=white) ![ApacheCassandra](https://img.shields.io/badge/cassandra-%231287B1.svg?style=for-the-badge&logo=apache-cassandra&logoColor=white) ![AmazonDynamoDB](https://img.shields.io/badge/Amazon%20DynamoDB-4053D6?style=for-the-badge&logo=Amazon%20DynamoDB&logoColor=white) ![Arango DB](https://img.shields.io/badge/ArangoDB-DDE072?style=for-the-badge&logo=arangodb&logoColor=white) ![Appwrite](https://img.shields.io/badge/Appwrite-%23FD366E.svg?style=for-the-badge&logo=appwrite&logoColor=white) ![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white) ![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white) ![Apache](https://img.shields.io/badge/apache-%23D42029.svg?style=for-the-badge&logo=apache&logoColor=white) ![Windicss](https://img.shields.io/badge/windicss-48B0F1.svg?style=for-the-badge&logo=windi-css&logoColor=white) ![Vue.js](https://img.shields.io/badge/vue.js-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D) ![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white) ![Badge Name](https://img.shields.io/badge/tRPC-%232596BE.svg?style=for-the-badge&logo=tRPC&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Svelte](https://img.shields.io/badge/svelte-%23f1413d.svg?style=for-the-badge&logo=svelte&logoColor=white) ![SolidJS](https://img.shields.io/badge/SolidJS-2c4f7c?style=for-the-badge&logo=solid&logoColor=c8c9cb) ![Socket.io](https://img.shields.io/badge/Socket.io-black?style=for-the-badge&logo=socket.io&badgeColor=010101) ![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white) ![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![React Query](https://img.shields.io/badge/-React%20Query-FF4154?style=for-the-badge&logo=react%20query&logoColor=white) ![React Hook Form](https://img.shields.io/badge/React%20Hook%20Form-%23EC5990.svg?style=for-the-badge&logo=reacthookform&logoColor=white) ![PNPM](https://img.shields.io/badge/pnpm-%234a4a4a.svg?style=for-the-badge&logo=pnpm&logoColor=f69220) ![Phoenix Framework](https://img.shields.io/badge/phoenixframework-%23FD4F00.svg?style=for-the-badge&logo=phoenixframework&logoColor=black) ![DjangoREST](https://img.shields.io/badge/DJANGO-REST-ff1709?style=for-the-badge&logo=django&logoColor=white&color=ff1709&labelColor=gray) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi) ![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB) ![Electron.js](https://img.shields.io/badge/Electron-191970?style=for-the-badge&logo=Electron&logoColor=white) ![Expo](https://img.shields.io/badge/expo-1C1E24?style=for-the-badge&logo=expo&logoColor=#D04A37) ![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white) ![Codeberg](https://img.shields.io/badge/Codeberg-2185D0?style=for-the-badge&logo=Codeberg&logoColor=white) ![DigitalOcean](https://img.shields.io/badge/DigitalOcean-%230167ff.svg?style=for-the-badge&logo=digitalOcean&logoColor=white) ![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white) ![Render](https://img.shields.io/badge/Render-%46E3B7.svg?style=for-the-badge&logo=render&logoColor=white) ![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white) ![Clojure](https://img.shields.io/badge/Clojure-%23Clojure.svg?style=for-the-badge&logo=Clojure&logoColor=Clojure) ![AssemblyScript](https://img.shields.io/badge/assembly%20script-%23000000.svg?style=for-the-badge&logo=assemblyscript&logoColor=white) ![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white) ![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![Erlang](https://img.shields.io/badge/Erlang-white.svg?style=for-the-badge&logo=erlang&logoColor=a90533) ![Haskell](https://img.shields.io/badge/Haskell-5e5086?style=for-the-badge&logo=haskell&logoColor=white) ![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white) ![Elixir](https://img.shields.io/badge/elixir-%234B275F.svg?style=for-the-badge&logo=elixir&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![Crystal](https://img.shields.io/badge/crystal-%23000000.svg?style=for-the-badge&logo=crystal&logoColor=white) ![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white) ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white) ![Scala](https://img.shields.io/badge/scala-%23DC322F.svg?style=for-the-badge&logo=scala&logoColor=white) ![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-%234D4D4D.svg?style=for-the-badge&logo=windows-terminal&logoColor=white) ![Bash Script](https://img.shields.io/badge/bash_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white) ![Ruby](https://img.shields.io/badge/ruby-%23CC342D.svg?style=for-the-badge&logo=ruby&logoColor=white) ![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white) ![Apache Groovy](https://img.shields.io/badge/Apache%20Groovy-4298B8.svg?style=for-the-badge&logo=Apache+Groovy&logoColor=white)
# 📊 GitHub Stats:
![](https://github-readme-stats.shion.dev/api?username=Rohankalhan&theme=dark&hide_border=false&include_all_commits=true&count_private=false)<br/>
![](https://streak-stats.demolab.com/?user=Rohankalhan&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.shion.dev/api/top-langs/?username=Rohankalhan&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

---
[![](https://komarev.com/ghpvc/?username=Rohankalhan&icon=0&color=0)](https://visitcount.itsvg.in)

  ## 💰 You can help me by Donating
  [![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/RohanKhan ) [![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/RohanKhan ) [![Patreon](https://img.shields.io/badge/Patreon-F96854?style=for-the-badge&logo=patreon&logoColor=white)](https://patreon.com/RohanKhan ) [![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/RohanKhan ) 

  
<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
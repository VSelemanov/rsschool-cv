# VLADISLAV SELEMANOV

## BASIC INFO

### Vladislav Selemanov, 24 y.o.

![Image of me](https://sun9-34.userapi.com/c628626/v628626892/2bcb/kfBAKvJNNTw.jpg)

## CONTACT INFO

E-mail: v.selemanov@mail.ru

Phone number: [+7(910)123-97-80](tel:89101239780)

Skype: [many14_95](skype:many14_95)

Social networks: [VK](https://vk.com/selemanov), [Instagram](https://www.instagram.com/selemanov_vlad/)

## SUMMARY

- IT Professional with 3+ years of experience in full stack development using node.js and React
- Good knowledge and practical experience with PostgreSQL, MySQL
- Good knowledge of HTML/CSS, cross-browser development
- Basic experience in Linux administration and setting up working environment
- In-depth understanding and experience in agile development environment (SCRUM)
- Good communication skills, experience in communication with customer, DEMO participation
- Motivation to grow and learn new programming languages and technologies

## SKILS

**Technologies and frameworks:**
JS, TS, NodeJS (HapiJS, HapiNES), ReactJS, HTML, CSS (SCSS)

**Source Control:**
GitLab, GitHub

**Methodology:**
BDD (TDD)

**Databases:**
MySQL, PostgreSQL, MongoDB

**OS:**
MacOS, Ubuntu, Windows

**IDE:**
VS Code, Intellij IDEA

**CMS:**
Joomla

## CODE EXAMPLE

```
import trycatcher from "../../utils/trycatcher";
import { server } from "../../server";
import { EntityName } from "./constants";
import { subscriptionGameStatuspath } from "../Room/constants";
import RoomMethods from "../Room";
...
import { IGamePart1 } from "../Room/interfaces";

const methods = {
    ...
    colorZone: trycatcher(
        async (zoneKey: string, teamKey: string) => {
        const Room: IRoom = await RoomMethods.colorZone(zoneKey, teamKey);
        const currentPart = Room.gameStatus.currentPart;

        if (currentPart === 1 && Room.gameStatus.part1.steps.length > 0) {
            const part: IGamePart1 = Room.gameStatus.part1;
            const step = part.steps[part.currentStep || 0];
            step.allowZones[teamKey] = step.allowZones[teamKey] - 1;
            if (step.allowZones[teamKey] === 0) {
            step.teamQueue.shift();
            }
            Room.markModified("gameStatus.part1.steps");
            await Room.save();
        }

        await server.server.publish(subscriptionGameStatuspath, Room.gameStatus);

        return "ok";
        },
        { logMessage: `${EntityName} colorZone method error` }
    ),
  ...
}

export const methods;

```

## WORK EXPERIENCE

**May, 2014 – August, 2014 – WEB-Developer**, ООО “Альфатехсервис” (Krasnodar)

**Project:**
Company landing pages

**Project Role:**
full-stack developer (junior)

**Tasks and Accomplishments:**

- Administration of company sites.
- Creation of new sites.
- Creation of advertising companies Yandex.Direct and Google Adwords.
- Conducting statistics on advertising companies.
- Analysis of advertising companies.
- Adjustments for advertising companies.
- Office Administration

**Technologies:**
PHP, JS, HTML, CSS

**Tools:**
Notepad++, FileZilla

**November, 2015 – September, 2018 – Software engineer**, ГБУ НО “Объединенная дирекция по реализации жилищных программ” (Nizhny Novgorod)

**Project:**
All company projects

**Project Role:**
full-stack developer

**Tasks and Accomplishments:**

- Developing projects based on Joomla 3+ for ministry of social policy
- Supporting users of these projects, DEMO for users
- Upgrade production projects

**Technologies:**
PHP, JS, HTML, CSS, MySQL, PostgreSQL

**Tools:**
Notepad++, SublimeText, FileZilla, PgAdmin, PHPMyAdmin

**October, 2018 – Until now – Programmer**, ГК “ЛАД” (Nizhny Novgorod)

**Projects:**
Unoto, ASE

**Project Role:**
junior frontend developer

**Tasks and Accomplishments:**

- pages layout
- local storage based on Redux
- async requests to project API

**Languages: Russian**

**Technologies:**
ReactJS, Redux, SCSS

**Tools:**
VS Code, Docker, Rancher, Git

**Project:**
Insurers

**Project Role:**
junior full-stack developer

**Tasks and Accomplishments:**

_Frontend:_

- pages layout (ReactTable)
- local storage based on Redux
- async requests to project API

_Backend:_

- Store data using MongoDB
- Creating API based on HapiJS

**Languages:**
Russian

**Technologies:**
ReactJS, NodeJS, Redux, SCSS

**Tools:**
VS Code, Docker, Rancher, Git, Robo3T, Mongo Express

**Project:**
building services platform

**Project Role:**
backend developer

**Tasks and Accomplishments:**

- Store data using PostgreSQL
- Creating API based on HapiJS

**Languages:**
Russian

**Technologies:**
NodeJS, TS, PostgreSQL

**Tools:**
VS Code, Docker, Rancher, Git, PgAdmin, Sequelize ORM

## LINKS TO COURCE CODE

- Test task for current job (the four-in-line game): [Four in line](https://github.com/VSelemanov/four-in-line)
- Last freelance game project (my role in project - backend developer): [NN Game](https://github.com/VSelemanov/NNGame)

## EDUCATION

**2011 – 2015:**
**Krasnodar college of electronic instrument making**

Computer technologies – Computer systems and computer complexes

**2015 – 2020:**
**Nizhny Novgorod State Technical University**

Computer science and computer engineering – Computing machines

**April, 24, 2018** - EPAM INSIDER (conference)

Learn some courses in [codecademy.com](https://codecademy.com) and [htmlacademy.ru](https://htmlacademy.ru) on start of my developer career.

## ENGLISH SKILLS

I studied English in college with extra lessons. At the end of this lessons, I passed the ESOL exam and I have a certificate confirm this fact (A1 level).

I have little expierence to communicating in English with people from UK. I can read technical documentation and speak on simple topics.

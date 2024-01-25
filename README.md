# fullstack-React-TypeScript

backend:
compose.yaml
docker compose up -d
docker ps -a

docker exec -it db psql -U postgres
\l
\dt
exit

mkdir backend
cd backend
npm init -y
npm i express prisma @prisma/client
npx prisma init

backend/.env
backend/prisma/schema.prisma
backend/index.js
npx prisma generate
node index.js
http://localhost:4000/test

backend/.dockerignore
backend/backend.dockerfile

docker compose build
docker compose up -d backend
docker ps -a

docker exec -it db psql -U postgres
\dt

docker exec -it backend npx prisma migrate dev --name init

docker exec -it db psql -U postgres
\dt

npx prisma studio
Chrome: http://localhost:5555

http://localhost:4000/users
{
  "name": "userfrompostman",
  "email": "userfrompostmanmail"
}

docker exec -it db psql -U postgres
\dt

insert into "User" (name, email) values ('frompsql', 'userfrompsqlmail');
select * from "User";


frontend:
cd ..
npx create-next-app@latest --no-git

What is your project named? frontend
TypeScript? Yes
EsLint? Yes
Tailwind CSS? Yes
Use the default directory structure? Yes
App Router? No (not needed for this project)
Customize the default import alias? No

cd frontend
npm i axios
npm run dev
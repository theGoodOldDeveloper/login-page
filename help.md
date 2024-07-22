npm install next-auth @next-auth/prisma-adapter @prisma/client bcrypt
npm install -g prisma

`app/
  api/
    auth/
      [...nextauth]/
        route.ts
  components/
    LoginForm.tsx
  page.tsx
prisma/
  schema.prisma
.env`

### setup .env

DATABASE_URL="postgresql://postgres:sususoft@localhost:5432/postgres?schema=public"
NEXTAUTH_SECRET="your-nextauth-secret"
GOOGLE_CLIENT_ID="your-google-client-id"
GOOGLE_CLIENT_SECRET="your-google-client-secret"

### init prisma project

npx prisma init
npx prisma init --datasource-provider postgresql

### create migrate

### before migrate

- create database
- right click
- Properties
- setup Owner (which is the same .env username) !!!!!!! 😎

  npx prisma migrate dev --name init

## USER

CREATE USER photovegh WITH PASSWORD 'sususoft';
GRANT ALL PRIVILEGES ON DATABASE logindb TO photovegh;
CREATE USER johndoe WITH PASSWORD 'sususoft';
GRANT ALL PRIVILEGES ON DATABASE logindb TO johndoe;

# NA SZOOOOOVAL 😈😈😈😈😈😈😈

## open psql

answers:
Server [localhost]: localhost
Database [postgres]: postgres
Port [5432]: 5432
Username [postgres]: postgres
Password for user postgres:
psql (16.3)
WARNING: Console code page (852) differs from Windows code page (1250)
8-bit characters might not work correctly. See psql reference
page "Notes for Windows users" for details.
Type "help" for help.

postgres=# CREATE DATABASE logindata;
postgres=# CREATE USER susu WITH PASSWORD 'Sususoft_0913';
postgres=# GRANT ALL PRIVILEGES ON DATABASE logindata TO susu;
postgres=# \q

## again open psql, connect logindata & susu

postgres=# \conninfo
info: connect details 😊

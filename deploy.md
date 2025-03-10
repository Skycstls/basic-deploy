1. Clona el repo en el vps
2. Configura el VPS para poder usar el proyecto

```bash
apt update
apt install  npm -y
npm install -g pm2
```

3. Entra en la carpeta del proyecto y descarga las dependencias

```bash
npm i
```
4. Comprueba que el servidor funciona

```bash
node server.js
```

5. Si funciona, instala y configura pm2

```bash
npm i -g pm2
pm2 start server.js --name mi-web
```

6. Asegurate de que `deploy.yml` hace pull donde debe y para y reinicia la aplicacion por el nombre establecido en pm2.
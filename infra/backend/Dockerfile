# Usamos una imagen oficial de Node.js como base
FROM node:20

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos de configuración y dependencias
COPY package*.json ./

# Instala las dependencias
RUN npm install

# Copia el resto del código fuente al contenedor
COPY . .

# Expone el puerto en el que corre tu backend (ajústalo si usas otro)
EXPOSE 3000

# Comando para iniciar la app
CMD ["node", "index.js"]

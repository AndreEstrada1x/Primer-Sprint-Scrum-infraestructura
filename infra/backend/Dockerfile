FROM node:20

# Crear directorio
WORKDIR /app

# Clonar el repo del backend directamente
RUN git clone https://github.com/Jonialen/EduVial-Backend.git .

# Instalar dependencias
RUN npm install

# Exponer el puerto (ajusta si es otro)
EXPOSE 3000

# Comando para ejecutar el servidor
CMD ["node", "index.js"]

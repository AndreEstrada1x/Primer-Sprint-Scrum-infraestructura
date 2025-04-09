FROM nginx:alpine

# Crear carpeta temporal
WORKDIR /tmp

# Clonar el frontend
RUN apk add git && \
    git clone https://github.com/Jonialen/EduVial-Frontend.git && \
    mv EduVial-Frontend/build/web /usr/share/nginx/html && \
    rm -rf /tmp/*

# Expone puerto estándar para web
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

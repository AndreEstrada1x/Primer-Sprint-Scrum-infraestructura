# Imagen oficial de Flutter
FROM cirrusci/flutter:latest

# Activar soporte web
RUN flutter config --enable-web

# Establecer directorio de trabajo
WORKDIR /app

# Copiar código fuente
COPY . .

# Obtener dependencias
RUN flutter pub get

# Compilar la aplicación Flutter web
RUN flutter build web

# Usar Nginx para servir la web
FROM nginx:alpine
COPY --from=0 /app/build/web /usr/share/nginx/html

EXPOSE 80
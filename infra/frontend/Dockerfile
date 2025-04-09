FROM cirrusci/flutter:3.19.6

WORKDIR /app

# Clonar el frontend desde GitHub
RUN git clone https://github.com/Jonialen/EduVial-Frontend.git .

# Instalar dependencias
RUN flutter pub get

# Compilar APK (puedes cambiar por build web o iOS si quieres)
RUN flutter build apk --release

# Dejar el APK disponible en una ruta compartida
CMD ["bash"]

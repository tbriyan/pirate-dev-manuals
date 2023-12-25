# Documentación para la instalación de oh my zsh

Oh My Zsh es un potente framework de código abierto para la terminal Zsh (Z shell), diseñado para mejorar la experiencia del usuario al utilizar la terminal en sistemas Unix. Ofrece una amplia gama de funciones, complementos y temas que hacen que trabajar en la línea de comandos sea más eficiente y agradable.

## Pasos de Instalación de Oh My Zsh:

### Requisitos previos:
- **Zsh:** Asegúrate de tener Zsh instalado en tu sistema. Puedes verificarlo escribiendo `zsh --version` en la terminal. Si no lo tienes, puedes instalarlo mediante el gestor de paquetes de tu sistema operativo.
- **Git:** Oh My Zsh se instala a través de Git, así que necesitarás tenerlo instalado también.

### Pasos:

1. **Instalar Oh My Zsh:**

   Abre tu terminal y ejecuta el siguiente comando para instalar Oh My Zsh:

   ```bash
   sudo apt install zsh
   ```

   ```bash
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```

   Este comando descargará el script de instalación de Oh My Zsh y lo ejecutará en tu sistema.

   ```bash
   chsh -s /bin/zsh
   ```
2. **Cambiar tu shell a Zsh:**

   Una vez finalizada la instalación, para cambiar tu shell predeterminada a Zsh, ejecuta:

   ```bash
   chsh -s $(which zsh)
   ```

   Se te solicitará tu contraseña para aplicar el cambio.

3. **Reiniciar la terminal:**

   Cierra la terminal actual y ábrela nuevamente para que los cambios surtan efecto.

4. **Personalizar Oh My Zsh (opcional):**

   Oh My Zsh viene con una variedad de temas y complementos preconfigurados. Puedes cambiar el tema editando el archivo `~/.zshrc` y modificando la variable `ZSH_THEME`. También puedes agregar complementos personalizados editando la sección `plugins` en el mismo archivo.

   Para aplicar los cambios realizados en el archivo `~/.zshrc`, ejecuta:

   ```bash
   source ~/.zshrc
   ```
   - **Personalización :** Existen varios plugins que se pueden instalar, entre los más importantes tenemos a `zsh-autosuggestions` entre otros, a continuación se muestra una guía de instalación:

   ```bash
    # Clonamos el siguiente repositorio en la ruta ~/.oh-my-zsh/custom/plugins

    git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

    # Agregamos el plugin a ~/.zshrc

    sudo nano ~/.zshrc

    # ...

    plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
    ```

Ahora deberías estar utilizando Oh My Zsh como tu shell predeterminada, con una amplia gama de características que mejorarán tu flujo de trabajo en la terminal.

Recuerda que Oh My Zsh es altamente personalizable, permitiendo que ajustes su configuración según tus necesidades y preferencias.
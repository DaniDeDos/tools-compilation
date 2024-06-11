<h1>Instalar Volta + Tools</h1>
 
<h2>Instalar <a href="https://docs.volta.sh/guide/getting-started">Volta</a></h2>

##### `Nota:` Volta actúa como una capa de abstracción que simplifica la gestión de versiones de Node.js y Yarn, permitiendo a los desarrolladores centrarse en el desarrollo sin tener que lidiar con la complejidad de mantener múltiples versiones de estas herramientas.

> ##### ⚠ Cambiar `~/.bashrc` por `~/.zshrc` si usa bash.

- Actualizar el sistema.
  ```js
  sudo pacman -Sy
  ```
- Descargar e instalar Volta.
  ```bash
  curl https://get.volta.sh | bash
  ```
- Exportar las variables al archivo del perfil de la shell.
  ```js
  echo 'export VOLTA_HOME="$HOME/.volta"' >> ~/.zshrc
  echo 'export PATH="$VOLTA_HOME/bin:$PATH"' >> ~/.zshrc
  ```
- Recargar el archivo del perfil.
  ```js
  source ~/.zshrc
  ```
- Comprobar versión.
  ```bash
  volta -v # O --version
  ```

<h2>Instalar <a href="https://nodejs.org/en/learn/getting-started/how-to-install-nodejs">Node.js</a></h2>

> ##### 💡 Recuerde que `node` integra `npm` y `npx`.

- Instalar Node.
  ```js
  volta install node
  ```
- Comprobar versión.

  ```bash
  npx -v
  npm -v
  node -v # --version
  ```

<h2>Instalar <a href="https://yarnpkg.com/getting-started/install">Yarn</a></h2>

> ##### ⚠ En algunos casos requiere `vpn`.

- Instalar yarn.
  ```js
  volta install yarn
  ```
- Comprobar versión.
  ```bash
  yarn -v # --version
  ```

---

<h2>Desinstalar Volta</h2>

- Desinstalar Volta.
  ```js
  rm -rf ~/.volta
  ```
- Eliminar las variables del archivo de perfil de la shell.
  ```js
  sed -i '/^ *export VOLTA_HOME="\$HOME\/\.volta"/d' ~/.zshrc
  sed -i '/^ *export PATH="\$VOLTA_HOME\/bin:\$PATH"/d' ~/.zshrc
  ```
- Recargar el archivo del perfil.
  ```js
  source ~/.zshrc
  ```

<h2>Referencias Oficliales</h2>
<ul>
  <li><a>Volta</a></li>
  <li><a>Volta</a></li>
  <li><a>Volta</a></li>
</ul>

<h2></h2>
<div align="right"><a>Página Principal</a></div>

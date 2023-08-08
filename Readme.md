# Custom 3D Shirt :tshirt:

Esse projeto fiz em um [tutorial](https://www.youtube.com/watch?v=tllZWCQZ9_0) que permite a personalização de camisetas em 3D. Os usuários podem criar camisetas  usando uma ferramenta de customização 3D. A aplicação apresenta uma interface interativa que permite ao usuário escolher cores, aplicar logos e fazer download da camiseta virtual.

### Conteúdo
- [Custom 3D Shirt :tshirt:](#custom-3d-shirt-tshirt)
    - [Conteúdo](#conteúdo)
  - [Tecnologias Utilizadas :hammer\_and\_wrench:](#tecnologias-utilizadas-hammer_and_wrench)
  - [Fluxo do Usuário :chains:](#fluxo-do-usuário-chains)
  - [Principais Componentes :computer:](#principais-componentes-computer)
    - [Home](#home)
    - [Customizer](#customizer)
    - [CameraRig](#camerarig)
    - [Shirt](#shirt)

## Tecnologias Utilizadas :hammer_and_wrench:

As principais tecnologias utilizadas neste projeto:

- **[React](https://pt-br.legacy.reactjs.org/)**: Uma biblioteca JavaScript para criar interfaces de usuário.
- **[TailwindCSS](https://tailwindcss.com/docs/guides/vite)**: Classes CSS "utilitárias" pré-definidas, permitindo estilizar elementos através da combinação de classes no HTML.
- **[Framer Motion](https://www.framer.com/motion/animate-presence/)**: Uma biblioteca de animação para React.
- **[React-three/fiber](https://docs.pmnd.rs/react-three-fiber/getting-started/installation)**: Uma biblioteca para criar gráficos 3D com React.
- **[React-three/drei](https://github.com/pmndrs/drei)**: Uma coleção de utilitários e componentes úteis para o react-three/fiber.
- **[Three.js](https://threejs.org/docs/index.html#manual/en/introduction/Creating-a-scene)**: Uma biblioteca JavaScript para criar e renderizar gráficos 3D.
- **[Valtio](https://valtio.pmnd.rs/docs/api/basic/proxy)**: Uma biblioteca de gerenciamento de estado para React.
- **[maath](https://github.com/pmndrs/maath)**: Uma biblioteca de interpolação e animação.

**Preview**

![Screenshot 3D Product Website](./client/public/github/Screenshot%202023-08-01%20at%2017-33-40%203D%20Product%20Website.png)

## Fluxo do Usuário :chains:

- Acessar a página inicial com o logotipo da aplicação e o botão "Customize It".
- Carregar a página de customização da camiseta ao clicar no botão.
- Personalizar a cor da camiseta.
- Fazer upload de imagens para aplicar como logo na camiseta.
- Alternar entre diferentes filtros.
- Fazer download da camiseta 3D.
- Visualização 3D aos movimentos do mouse durante a customização da camiseta.

## Principais Componentes :computer:

### Home

- O componente `Home` é a página inicial da aplicação. Ele contém a animação de entrada e apresenta o logotipo da aplicação e um botão "Customize It". Quando o botão é clicado, o estado "intro" é atualizado para `false`, e o componente "Customizer" é exibido.

### Customizer

O componente `Customizer` é a parte principal da aplicação, onde a customização da camiseta acontece.

- `EditorTabs`: Permitem ao usuário escolher entre as opções de customização, como seleção de cor e upload de imagens.
- `FilterTabs`: Permitem ao usuário alternar entre os tipos de estilização (logo e estilizado) para a camiseta.
- `ColorPicker`: Permite ao usuário selecionar a cor da camiseta.
- `FilePicker`: Permite ao usuário fazer upload de uma imagem para aplicar como logo na camiseta.

### CameraRig

- O componente `CameraRig` controla a posição e rotação da câmera 3D na cena. Ele usa a biblioteca `maath` para aplicar animações suaves à câmera, dependendo do estado da aplicação.

### Shirt

- O componente `Shirt` renderiza a camiseta 3D na tela. Ele usa a biblioteca `react-three/drei` para carregar a malha e os materiais da camiseta a partir de um arquivo `.glb`.

---
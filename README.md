<div id="top"></div>

<div align="center">
	<a href="https://github.com/Link-Wolf/FdF" title="Go to GitHub repo"><img src="https://img.shields.io/static/v1?label=Link-Wolf&message=FdF&color=blue&logo=github&style=for-the-badge" alt="Link-Wolf - FdF"></a>
	<a href="https://"><img src="https://img.shields.io/badge/42_grade-125_%2F_100-2ea44f?style=for-the-badge" alt="42 grade - 125 / 100"></a>
	<a href="https://"><img src="https://img.shields.io/badge/Year-2022-ffad9b?style=for-the-badge" alt="Year - 2022"></a>
	<a href="https://github.com/Link-Wolf/FdF/stargazers"><img src="https://img.shields.io/github/stars/Link-Wolf/FdF?style=for-the-badge&color=yellow" alt="stars - FdF"></a>
	<a href="https://github.com/Link-Wolf/FdF/network/members"><img src="https://img.shields.io/github/forks/Link-Wolf/FdF?style=for-the-badge&color=lightgray" alt="forks - FdF"></a>
	<a href="https://github.com/Link-Wolf/FdF/issues"><img src="https://img.shields.io/github/issues/Link-Wolf/FdF?style=for-the-badge&color=orange" alt="issues - FdF"></a>
	<a href="https://www.apple.com/macos/" title="Go to Apple homepage"><img src="https://img.shields.io/badge/OS-macOS-blue?logo=apple&logoColor=white&style=for-the-badge&color=9cf" alt="OS - macOS"></a>
</div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a>
    <img src="https://www.42mulhouse.fr/wp-content/uploads/2022/06/logo-42-Mulhouse-white.svg" alt="Logo" width="192" height="80">
  </a>

  <h3 align="center">FdF</h3>

  <p align="center">
	  <em>U said wire ?</em><br/>
    Wireframe modeling
    <br />
    <br />
    <a href="https://github.com/Link-Wolf/FdF/issues">Report Bug</a>
    ·
    <a href="https://github.com/Link-Wolf/FdF/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<div align="center">
  <a>
    <img src="https://media.discordapp.net/attachments/453159761639112706/998876414004703292/unknown.png" alt="FdF header">
  </a>
</div>
</br>

This project consists of graphically creating the schematic representation
of raised terrain
The program takes a file `.fdf` as a parameter and show the 3D representation of the file content</br>
To do this, we're allowed to use our [libft](https://github.com/Link-Wolf/libft), [get next line](https://github.com/Link-Wolf/get_next_line), the C `math` library, and a tiny local graphic library : the [minilibx](https://harm-smits.github.io/42docs/libs/minilibx/introduction.html) (also called mlx)

- The file contains `n` lines with the same size
- The file must contain only integers, separated by space
- Each integer represents the altitude of the related point
- Each point must be joined to the 2 / 3 / 4 others around it

This is an example of a valid file
```
	0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
	0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
	0 0 1 1 0 0 1 1 0 0 0 1 1 1 1 1 0 0 0
	0 0 1 1 0 0 1 1 0 0 0 0 0 0 0 1 1 0 0
	0 0 1 1 0 0 1 1 0 0 0 0 0 0 0 1 1 0 0
	0 0 1 1 1 1 1 1 0 0 0 0 1 1 1 1 0 0 0
	0 0 0 1 1 1 1 1 0 0 0 1 1 0 0 0 0 0 0
	0 0 0 0 0 0 1 1 0 0 0 1 1 0 0 0 0 0 0
	0 0 0 0 0 0 1 1 0 0 0 1 1 1 1 1 1 0 0
	0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
	0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0
```

We have to render the result in an isometric projection and be able to close the window either by the red cross or by press `ESC`

### Bonus features

- Include an additional projection (you can switch by pressing `TAB`)
- Implement zoom in and out (scroll wheel)
- Implement translation (press `WASD`)
- Implement at least one rotation (I added all of them by pressing `JL`/`IK`/`UO`)
- Add an additional bonus of my choice. I added colors for the wireframe when the map is big enough. The next picture is an illustration of it with a big, big map

<div align="center">
  <a>
    <img src="https://media.discordapp.net/attachments/453159761639112706/998876964981051443/unknown.png" alt="FdF header">
  </a>
</div>
</br>

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

It's a simple C program but
<span style="color:red">/!\\ sadly the mlx used is only available locally on 42 iMacs /!\\</span></br>
**However** you can use the [improved one](https://github.com/codam-coding-college/MLX42), it will *just* need to edit some includes, the [Makefile](https://github.com/Link-Wolf/FdF/blob/master/Makefile) and maybe some other little things

### Prerequisites

Having a C compiler like cc, gcc or clang</br>
Be on a 42 iMac or get the MLX42 described above

### Installation
Assuming you are on a 42 iMac</br>
If you use the MLX42, use its [documentation](https://github.com/codam-coding-college/MLX42)
1. Clone the repo
   ```sh
   git clone https://github.com/Link-Wolf/FdF.git
   ```
2. Compile FdF
   ```sh
   cd FdF; make
   ```
3. Execute the program with a `.fdf` file
   ```sh
   ./fdf [your file].fdf
   ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Test this FdF with any map you want !</br>
The first picture is the result from this command :
```sh
   ./fdf 42.fdf
```

*(You can find some example [maps](https://github.com/Link-Wolf/FdF/tree/master/maps) in the maps folder)*

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Add all bonus features
- [x] Add some examples maps
- [x] Add back to top links

See the [open issues](https://github.com/Link-Wolf/FdF/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Mail : xxxxxxx@student.42mulhouse.fr

Project Link: [https://github.com/Link-Wolf/FdF](https://github.com/Link-Wolf/FdF)

<p align="right">(<a href="#top">back to top</a>)</p>

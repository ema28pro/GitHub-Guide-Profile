# 01. Introducción al Control de Versiones

[🏠 Volver al Índice](./README.md) | [Siguiente Módulo: Fundamentos de Git ➡️](./02-fundamentos-de-git.md)


## 🎯 ¿Por qué Necesitamos el Control de Versiones?

Imagina que estás escribiendo un trabajo importante o desarrollando una aplicación. Probablemente hayas guardado copias como:
- `proyecto_final.zip`
- `proyecto_final_v2.zip`
- `proyecto_final_ahora_si_bueno.zip`
- `proyecto_final_definitivo_final.zip`

En el desarrollo de software, este enfoque manual es caótico, propenso a errores e insostenible. Para solucionar precisamente estos problemas nacieron los **Sistemas de Control de Versiones (VCS)**, con **[Git](https://git-scm.com/)** como el estándar indiscutible de la industria a nivel mundial.

Un sistema de control de versiones permite:
1. **Historial completo**: Revertir archivos o proyectos enteros a cualquier estado anterior de forma instantánea.
2. **Comparación clara**: Ver exactamente qué líneas cambiaron a lo largo del tiempo y quién hizo cada cambio.
3. **Seguridad**: Saber con total certeza quién, cuándo y por qué introdujo una modificación o un error.
4. **Trabajo en equipo**: Permitir que decenas de programadores trabajen en paralelo sin pisarse ni sobrescribir el trabajo ajeno.


## ☁️ Plataformas de Alojamiento en la Nube

Para respaldar tu código en internet, compartirlo y colaborar con personas de todo el mundo, existen diversos servicios de alojamiento de repositorios Git:

- **[GitHub](https://github.com/)**: La plataforma más popular y grande del mundo (propiedad de Microsoft).
- **[GitLab](https://about.gitlab.com/)**: Plataforma completa con potentes herramientas de CI/CD y opción autoalojada.
- **[Bitbucket](https://bitbucket.org/)**: Servicio desarrollado por Atlassian, muy integrado con Jira y Trello.
- **[Gitea](https://about.gitea.com/)**: Plataforma ligera, de código abierto y fácil de autoalojar en tus propios servidores.
- **[Codeberg](https://codeberg.org/)**: Alternativa comunitaria, sin fines de lucro y orientada a la privacidad y el software libre.
- **[NotABug](https://notabug.org/)**: Plataforma de colaboración enfocada exclusivamente en proyectos y software libre (*libre software*).


## ⚖️ Git vs. GitHub: ¿En qué se diferencian?

Es muy común que los principiantes confundan ambos conceptos:

| Característica | 🛠️ Git | 🐙 GitHub |
| :--- | :--- | :--- |
| **¿Qué es?** | Software de control de versiones distribuido. | Plataforma web en la nube basada en Git. |
| **Creador** | Linus Torvalds (creador de Linux) en 2005. | Chris Wanstrath, P. J. Hyett, Tom Preston-Werner (2008). Adquirido por Microsoft en 2018. |
| **Dónde se ejecuta** | Localmente en tu computadora (terminal o GUI). | En servidores remotos en la nube. |
| **Función principal** | Registrar el historial de cambios de tu código. | Alojar repositorios, facilitar colaboración, CI/CD y gestión de proyectos. |
| **Conexión a Internet** | **No requerida** para la mayoría de operaciones. | **Requerida** para sincronizar y colaborar. |
| **Alternativas** | Mercurial, SVN (Subversion). | GitLab, Bitbucket, Gitea, Codeberg, NotABug. |

> [!IMPORTANT]
> **Git funciona sin GitHub**, pero **GitHub no puede existir sin Git**. Git es el motor interno; GitHub es la plataforma en la nube que lo potencia y facilita la colaboración social.

---

[🏠 Volver al Índice](./README.md) | [Siguiente Módulo: Fundamentos de Git ➡️](./02-fundamentos-de-git.md)

# Introduzione

Tutte le volte che voglio creare delle ***slide* HTML** - come [queste](https://revealjs.com/) - basate sul meraviglioso [**reveal.js**](https://github.com/hakimel/reveal.js), **perdo** tanto **tempo** a ricordami **come si faccia**.<br>
È facile, sul sito ufficiale è ben spiegato, ma "sono di coccio" e **non riesco (quasi) mai a farlo presto e bene**.

Questo repository nasce per **risolvere** questo mio **problema**: lo scarico in una nuova cartella e devo soltanto pensare al file *markdown* in cui inserire il contenuto delle slide.

[![](./imgs/esempio_01.png)](https://aborruso.github.io/revealjs-start)



# Come fare

- **Scarica** lo zip del **repository**, da qui <https://github.com/aborruso/revealjs-start/archive/master.zip>;
- **decomprimilo** in una cartella;
- **modifica** e arrichischi i **contenuti** delle slide, lavorando sul file `markdown` di esempio denominato **`input.md`**, che trovi nella radice della cartella;
- **guarda** le tue **slide**, lanciando un ***server web***, puntando alla cartella e aprendo il file `index.html`.
  - se hai python3 installato, puoi lanciare `python3 -m http.server`

# Note

## Configurazione

Per impostare i parametri di configurazione di `reveal.js`, si può aprire il file [`index.html`](./index.html) e modificare la parte

```html
<script>

  // More info https://github.com/hakimel/reveal.js#configuration
  Reveal.initialize({
    controls: true,
    progress: true,
    center: true,
    hash: true,
    slideNumber: true,

    transition: 'slide', // none/fade/slide/convex/concave/zoom

    // More info https://github.com/hakimel/reveal.js#dependencies
    dependencies: [
      { src: 'plugin/markdown/marked.js', condition: function () { return !!document.querySelector('[data-markdown]'); } },
      { src: 'plugin/markdown/markdown.js', condition: function () { return !!document.querySelector('[data-markdown]'); } },
      { src: 'plugin/highlight/highlight.js', async: true },
      { src: 'plugin/search/search.js', async: true },
      { src: 'plugin/zoom-js/zoom.js', async: true },
      { src: 'plugin/notes/notes.js', async: true }
    ]
  });

</script>
```

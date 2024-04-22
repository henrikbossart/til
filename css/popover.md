### 3 lines to make tooltips/popovers stay anchored

3 lines of CSS to make your tooltips/menus stay in view 🤯
(Check it! 👇)

```css
[popover] {
top: anchor(top);
left: anchor(right);
position-try-options: flip-block, flip-inline;
}

```

Responds to scroll, layout change, etc.


Source: https://twitter.com/jh3yy/status/1778946758510260727?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E1778946758510260727%7Ctwgr%5E553e996bf8f04eff378b746601ce34d24a82aace%7Ctwcon%5Es1_&ref_url=https%3A%2F%2Fwww.kode24.no%2Fartikkel%2Fnextjs-142-er-nok-ikke-bare-jeg-som-blir-frustrert-av-mangelfulle-feilmeldinger%2F81287336
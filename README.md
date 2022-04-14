# understanding vue mount for a blog
 this repo is about understand https://unpkg.com/vue@3.2.32/dist/vue.global.js and how does it interact with script

## Notes

- there are actually unmount function which is interesting
- flushJobs(seen) make sure that parent come first and skip unmounted components
- checkRecursiveUpdates(seen, fn) check if recursions excced the limited amount and stop it if it exceed it
- this article https://www.jscodetips.com/index.php/examples/how-to-handle-initializing-and-rendering-subviews-in-backbone-js helped me with understanding rerender(id, newRender) 
- rerender(id, newRender) it's useful for `<slot />` so I will check this later when i start using slot and it  
- reload(id, newComp) this one handle updating the page and has interesting fallback
- what is subtree https://stackoverflow.com/questions/36700148/what-is-a-subtree-when-referring-to-the-dom-in-javascript
- there is process function that happens before mount() 
- suspence is used as fallback(), experimental feature and its API will likely change

### Notes related to javascript languages
- try{}, catch{}, finaly{
  finally will run regardless of try result
}
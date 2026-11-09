# library

Odin Project: Library
planning stuff:

handling data:
object usage: we can have a array library, then just push 'book' objects into it so like
-- const library = []; library.push(book) for later

object constructors (use class keyword instead): make the book objects something like
class Book { constructor({ blablabla }) {this.blablabla = blabla;}}
to access them smmin like:
-- library.forEach(book => function());
-- the function: console.table(book), and we can render it in html there aswell

forms: for book object data
-- we can use new FormData() constructor, turns inputs into a [key, value] list
-- reading on it, it only scans inputs with a name, ex. input name='title'
-- and to turn it into an object we can use Object.fromEntries()
-- opposite of that is Object.entries(), turns objects into key values seems
-- really good for allowing use of rlly useful array methods, then u can make it into an obj again
hmm to do this probably: (add e.preventDefault() aswell)
form.addEventListener('submit', (e) => {bookdata = Object.fromEntries(new FormData(form));
const book = new Book(bookdata); library.push(book); console.table(library);})

~~look into js json methods and local storage:
~~saving: localStorage.setItem('savedLibrary', JSON.stringify(library));
~~loading: const rawLibraryData = localStorage.getItem('savedLibrary');
~~if(rawLibraryData) {const bookDataArray = JSON.parse(rawLibraryData);
~~bookDataArray.forEach(book => library.push(new Book(book)))}

found shiny new thing, looking into indexedDB
WIP

# MA274 Final Presentation

- `proof.tex` is where we write the proof 
- `index.md` is where we write the presentation

## How To Use

###  Clone this repository

```bash 
git clone https://github.com/ngvt1n/ma274finalproject
cd ma27finalproject
```

###  Install [`marp-cli`](https://github.com/marp-team/marp-cli): 

#### macOS / Linux: **[Homebrew](https://brew.sh/)**

```bash
brew install marp-cli
```

#### Windows: **[Scoop](https://scoop.sh/)**

```cmd
scoop install marp
```

#### Online usage: If already have NodeJS: 
```bash 
# Convert slide deck into HTML
npx @marp-team/marp-cli@latest -I -w -s # (see command below)
```

###  Preview the presentation in the browser

In this directory: 
```bash 
marp -I . -w -s
```

In which: 
- `I .`: let this directory be the input
- `-w`: watch for input changes in index.md 
- `-s`: server mode, preview in browser

Then, go to browser `[http://localhost:8000](http://localhost:8000)`

## Credits 
- Uses [Academic Theme](https://github.com/kaisugi/marp-theme-academic/blob/main/demo.md?plain=1) 

---

For any questions contact Tin

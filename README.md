<h1 align='center'>
  🜾 <br>
  Coventry Grove Builders Association
</h1>

<p align='center'>
  Home Base for all Coventry Grove Building Projeckts
</p>

## Checklist

When you use this template, try to follow the checklist to update your info properly 

- [ ] add Logo to index.vue

<br>

<p align='center'>
<a href="https://cgba.netlify.app/">Live Demo</a>
</p>

<br>


See [Myriad Checklist](./MYRIAD_CHECKLIST.md) for current status as a Myriad Central Node (as this is the template, you'll see where we're at ecosystem wise as we will start everything here and migrate out to other sites as it stablizes)



## Usage

### Development

Just run and visit http://localhost:3333

```bash
pnpm dev
```

### Build

To build the App, run

```bash
pnpm build
```

And you will see the generated file in `dist` that ready to be served.

### Deploy on Netlify

First, initialize as a Netlify site

```
ntl init
```

Then just build and deploy

```
ntl build
ntl deploy
```

Then, after review, deploy to production with

```
ntl deploy --prod
```


<script>
  import logo from './assets/images/logo-universal.png';
  import {Greet} from '../wailsjs/go/main/App.js';

  let resultText = "Please enter your name below 👇"
  let name

  function greet() {
    Greet(name).then(result => resultText = result)
  }
</script>

<main>
  <div class="hero min-h-screen" style="background-image: url(https://placeimg.com/640/480/any/grayscale);">
    <div class="hero-overlay bg-opacity-80"></div>

    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <h1 class="mb-5 text-5xl font-bold">Hello there</h1>
        <p class="mb-5">Provident cupiditate voluptatem et in. Quaerat fugiat ut assumenda excepturi exercitationem quasi. In deleniti eaque aut repudiandae et a id nisi.</p>
        <div class="card flex-shrink-0 w-full shadow-2xl bg-base-100">
          <div class="card-body">
            <div type="label" class="label" id="result">{resultText}</div>
            <input type="text" autocomplete="off" placeholder="name" class="input input-bordered" id="name" bind:value={name} />
            <button class="btn" on:click={greet}>Greet</button>
            <button class="btn btn-primary">One</button>
            <button class="btn btn-secondary">Two</button>
          </div>
          <h1 class="text-3xl font-bold underline">
            Hello world!!!!!!
          </h1>
        </div>
      </div>
    </div>    

  </div>
</main>
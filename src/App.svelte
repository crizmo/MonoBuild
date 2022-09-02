<script>
  // @ts-ignore
  import unit from '../src/assets/mono.svg';

  let items = [1,2,3,'Train']
  let item = items[Math.floor(Math.random()*items.length)]
  console.log(item)

  let one = 'https://cdn.discordapp.com/attachments/784621182249992253/1014597714530545734/one.png'
  let two = 'https://cdn.discordapp.com/attachments/784621182249992253/1014597714933190666/two.png'
  let three = 'https://cdn.discordapp.com/attachments/784621182249992253/1014597715302285312/three.png'
  let train = 'https://cdn.discordapp.com/attachments/784621182249992253/1014597715721736223/train.png'

  let monoSvg = unit
  
</script>

<main>
  <h1>Random Item</h1>
  <button on:click={() => {
    item = items[Math.floor(Math.random()*items.length)]
    if (item === 'Train') {
      monoSvg = train
    } else if (item === 1) {
      monoSvg = one
    } else if (item === 2) {
      monoSvg = two
    } else if (item === 3) {
      monoSvg = three
    } 
  }}>Random</button>

  <img src={monoSvg} alt="mono" />
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }
</style>

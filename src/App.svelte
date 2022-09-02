<script>
  // @ts-ignore
  import unit from '../src/assets/MonoBuild.svg';
  import '../src/mono.css';

  let items = [1,2,3,'Train']
  let item = items[Math.floor(Math.random()*items.length)]

  let one = 'https://cdn.discordapp.com/attachments/784621182249992253/1015131005222391849/unknown.png'
  let two = 'https://cdn.discordapp.com/attachments/784621182249992253/1015131109144670249/unknown.png'
  let three = 'https://cdn.discordapp.com/attachments/784621182249992253/1015131192166715392/unknown.png'
  let train = 'https://cdn.discordapp.com/attachments/784621182249992253/1015130927619379281/unknown.png'

  let monoSvg = unit

  function pog(){
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
    console.log(item)
  }

  function load(){
    for (let i = 0; i < 5; i++) {
      setTimeout(() => {
        monoSvg = one
      }, i * 1000)
      setTimeout(() => {
        monoSvg = two
      }, (i * 1000) + 200)
      setTimeout(() => {
        monoSvg = three
      }, (i * 1000) + 400)
      setTimeout(() => {
        monoSvg = train
      }, (i * 1000) + 600)
    }
    setTimeout(() => {
      pog()
    } , (5 * 1000) + 800)
  }
  
</script>

<main>
  <h1>MonoBuild</h1>
  <img src={monoSvg} alt="mono" />
  <button on:click={load}>Build</button>
</main>

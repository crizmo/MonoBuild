<script>
  // @ts-ignore
  import unit from '../src/assets/MonoBuild.svg';

  let items = [1,2,3,'Train']
  let item = items[Math.floor(Math.random()*items.length)]
  // console.log(item)

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

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 100px;
  }

  h1 {
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 1rem;
  }

  img {
    width: 100%;
    height: auto;
  }

  button {
    font-size: 1.2rem;
    font-weight: bold;
    border: none;
    background: none;
    color: rgb(0, 0, 0);
    padding: 0.5rem 1rem;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.2s ease-in-out;
    margin-top: 10px;
    background-color: #fff;
  }

  button:hover {
    background-color: #f5f5f5;
    transition: all 0.2s ease-in-out;
    transform: scale(1.05);
  }
</style>

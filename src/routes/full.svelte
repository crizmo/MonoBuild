<script>
    // @ts-ignore
    import unit from "../assets/MonoBuild.svg";
    import "/src/mono.css";

    let items = [1, 2, 3, "Train"];
    let item;

    let one =
        "https://cdn.discordapp.com/attachments/784621182249992253/1015131005222391849/unknown.png";
    let two =
        "https://cdn.discordapp.com/attachments/784621182249992253/1015131109144670249/unknown.png";
    let three =
        "https://cdn.discordapp.com/attachments/784621182249992253/1015131192166715392/unknown.png";
    let train =
        "https://cdn.discordapp.com/attachments/784621182249992253/1015130927619379281/unknown.png";

    let monoSvg = unit;

    function singleAud() {
        var single = new Audio("https://media.vocaroo.com/mp3/1okRPHtAoFOl");
        single.play();
    }

    function finalAud() {
        var final = new Audio("https://media.vocaroo.com/mp3/1frfuxBZ4LzR");
        final.play();
    }

    function pog() {
        item = items[Math.floor(Math.random() * items.length)];
        // console.log(item)
        if (item === "Train") {
            monoSvg = train;
        } else if (item === 1) {
            monoSvg = one;
        } else if (item === 2) {
            monoSvg = two;
        } else if (item === 3) {
            monoSvg = three;
        }
    }

    function finalRun() {
        for (let i = 0; i < 3; i++) {
            setTimeout(() => {
                monoSvg = one;
            }, i * 550);
            setTimeout(() => {
                monoSvg = two;
            }, i * 550 + 200);
            setTimeout(() => {
                monoSvg = three;
            }, i * 550 + 400);
            setTimeout(() => {
                monoSvg = train;
            }, i * 550 + 600);
        }
        // console.log("total time in seconds: " + (3 * 550) / 1000)
    }

    function load() {
        for (let i = 0; i < 5; i++) {
            setTimeout(() => {
                monoSvg = one;
                singleAud();
            }, i * 1000);
            setTimeout(() => {
                monoSvg = two;
                singleAud();
            }, i * 1000 + 200);
            setTimeout(() => {
                monoSvg = three;
                singleAud();
            }, i * 1000 + 400);
            setTimeout(() => {
                monoSvg = train;
                singleAud();
            }, i * 1000 + 600);
        }

        setTimeout(() => {
            finalAud();
            finalRun();
        }, 5000);

        setTimeout(() => {
            pog();
        }, 7 * 1000 + 50);
    }
</script>

<main>
    <h1>MonoBuild</h1>
    <img src={monoSvg} alt="mono" />
    <button on:click={load}>Build</button>
</main>

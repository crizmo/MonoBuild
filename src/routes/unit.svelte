<script>
    // @ts-ignore
    // @ts-ignore
    // @ts-ignore
    import unit from "../assets/MonoBuild.svg";
    import "/src/mono.css";

    // @ts-ignore
    import one from "../assets/modes/one.svg";
    // @ts-ignore
    import two from "../assets/modes/two.svg";
    // @ts-ignore
    import three from "../assets/modes/three.svg";
    // @ts-ignore
    import train from "../assets/modes/rail.svg";

    let items = [1, 2, 3, "Train"];
    let item;

    // let one =
    //     "https://media.discordapp.net/attachments/1014539635805929492/1107176426047819786/one.png";
    // let two =
    //     "https://cdn.discordapp.com/attachments/1014539635805929492/1107176425838100500/two.png";
    // let three =
    //     "https://cdn.discordapp.com/attachments/1014539635805929492/1107176425611603988/three.png";
    // let train =
    //     "https://cdn.discordapp.com/attachments/1014539635805929492/1107176425326399580/rail.png";

    let monoSvg =
        "https://cdn.discordapp.com/attachments/1014539635805929492/1107176426270109768/blank.png";

    function FullAud() {
        var full = new Audio("https://media.vocaroo.com/mp3/1kxpPMbBbBVO");
        full.play();
    }

    function pog() {
        item = items[Math.floor(Math.random() * items.length)];
        console.log(item);
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
        for (let i = 0; i < 4; i++) {
            setTimeout(() => {
                monoSvg = one;
            }, i * 700);
            setTimeout(() => {
                monoSvg = two;
            }, i * 700 + 200);
            setTimeout(() => {
                monoSvg = three;
            }, i * 700 + 400);
            setTimeout(() => {
                monoSvg = train;
            }, i * 700 + 600);
            setTimeout(() => {
                monoSvg = one;
            }, i * 700 + 800);
        }
        // console.log("total time in seconds: " + (3 * 550) / 1000)
    }

    function load() {
        FullAud();
        for (let i = 0; i < 3; i++) {
            setTimeout(() => {
                monoSvg = one;
            }, i * 750);
            setTimeout(() => {
                monoSvg = two;
            }, i * 750 + 200);
            setTimeout(() => {
                monoSvg = three;
            }, i * 750 + 400);
            setTimeout(() => {
                monoSvg = train;
            }, i * 750 + 600);
        }

        setTimeout(() => {
            finalRun();
        }, 2000);

        setTimeout(() => {
            pog();
        }, 5 * 1000 + 50);
    }

    function auction() {
        for (let i = 0; i < 22.228; i++) {
            setTimeout(() => {
                monoSvg = one;
            }, i * 900);
            setTimeout(() => {
                monoSvg = two;
            }, i * 900 + 200);
            setTimeout(() => {
                monoSvg = three;
            }, i * 900 + 400);
            setTimeout(() => {
                monoSvg = train;
            }, i * 900 + 600);
        }
        console.log("total time in seconds: " + (22.228 * 900) / 1000);
    }
</script>

<main>
    <h1>MonoBuild</h1>
    <img src={monoSvg} alt="mono" />

    <div
        class="box"
        style="display: flex; justify-content: space-between; width: 100%; margin-top: 20px; margin-bottom: 20px;"
    >
        <div
            class="left"
            style="width: 100%; display: flex; justify-content: center; align-items: center; flex-direction: column;"
        >
            <button on:click={load}>Build</button>
        </div>
    </div>
</main>

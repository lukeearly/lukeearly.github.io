<script>
    export let id;
    export let side = "left";
</script>

<style>
    span.sidenote {
        counter-increment: sidenote-count;
    }

    span.sidenote:hover {
        color: rgb(214, 20, 20);
    }

    label { 
        /* text-decoration: dotted underline 2px; */
        /* border: 2px dotted rgba(51, 51, 51, 0.4); */
        border: 2px solid rgba(0, 0, 0, 0);
        border-radius: 0.3em;
        padding: 0.05em;
        background-color: #e8e8e8;
    }

    span.sidenote:hover label {
        /* text-decoration: underline 2px; */
        border-style: solid;
        border-color: rgba(214, 20, 20, 0.7);
        /* border: 2px solid rgba(214, 20, 20, 0.5); */
    }

    input {
        display: none;
    }

    aside {
        /* background-color: #f8f8f8; */
        /* padding: 1em; */
        /* border-radius: 1em; */
        /* border: 1px solid rgba(51, 51, 51, 0.2); */
        color: inherit;
        position: relative;
        font-size: 0.8rem;
        font-weight: 400;
    }

	@media (max-width: 1000px) {
        aside {
            background-color: #f0f0f0;
            padding: 1em;
            border-radius: 8px;
            border: 1px solid rgba(51, 51, 51, 0.2);

            width: 75%;

            margin: 0.5em auto;

            display: none;
            height: 0;
            transition: height 400ms linear;
        }

        input:checked ~ aside {
            display: block;
            height: auto;
        }

        label span::after {
            content: "↓";
        }

        input:checked ~ label span::after {
            content: "↑";
        }
    }

	@media (min-width: 1000px) {
        label::after {
            content: counter(sidenote-count);
            font-size: .7em;
            font-weight: bold;
            vertical-align: super;
        }

        aside::before {
            content: counter(sidenote-count)". ";
            font-weight: bold;
        }

        aside {
            margin-bottom: 1em;
            padding: 0;
        }

        aside.left {
            width: 20vw;
            margin-left: calc(-20vw - 5em);
            float: left;
            clear: left;

            padding-right: 1em;
            border-right: 2px solid rgba(51, 51, 51, 0.2);
        }

        aside.right {
            width: 20vw;
            margin-right: calc(-20vw - 5em);
            float: right;
            clear: right;

            padding-left: 1em;
            border-left: 2px solid rgba(51, 51, 51, 0.2);
        }
	}

    /* span.num {
        position: relative;
        margin-left: -4em;
        float: left;
        clear: left;
    } */
</style>

<span class="sidenote">
    <input type="checkbox" id="toggle:{id}">
    <label for="toggle:{id}">
        <!-- <a id="snref:{id}" href="#sn:{id}"><slot name="summary"></slot></a> -->
        <span><slot name="summary"></slot></span>
    </label>
    <aside class="body-text {side}" id="sn:{id}">
        <!-- <a href="#sn:{id}">#</a> -->
        <slot></slot>
    </aside>
</span>
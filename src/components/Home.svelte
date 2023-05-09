<script>
    var n = [1, 1, 1, 1, 1, 1, 1, 1, 1]
</script>

<main>
    <div style="height: 100%; width: 75%; position: absolute; top: 0; left: 0;" class="p-3">
        <div style="height: 100%" class="shadow-none p-3 bg-light rounded">
            <div style="height: 100%; overflow: auto">
                <div class="p-3 bg-body rounded" style="width: 100%">
                    <img src="https://em-content.zobj.net/thumbs/320/twitter/322/nerd-face_1f913.png" style="width: 50px; heigth: 50px" class="m-3" alt="nerd">
                    <h5 style="display: inline" class="">Nerd</h5>
                    <textarea class="form-control mb-3" style="height: 100px"></textarea>
                    <button class="form-control btn btn-primary" style="m-3">Publicar</button>
                </div>
                {#each n as i}
                <div class="p-3 mt-3 bg-body rounded" style="width: 100%">
                    <img src="https://em-content.zobj.net/thumbs/320/twitter/322/nerd-face_1f913.png" style="width: 50px; heigth: 50px" class="m-3" alt="nerd">
                    <h5 style="display: inline" class="">Nerd</h5>
                    <p class="m-3">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
                    <img src="https://i.kym-cdn.com/entries/icons/original/000/039/761/nerdfacecover.jpg" style="width: 100%" alt="nerd">
                </div>
                {/each}
            </div>
        </div>
    </div>
    <div style="height: 100%; width: 25%; position: absolute; top: 0; right: 0;" class="p-3">
        <div style="height: 100%" class="shadow-none p-3 bg-light rounded">
            <div style="height: 50%; overflow: auto">
                {#each n as i}
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img src="https://em-content.zobj.net/thumbs/320/twitter/322/nerd-face_1f913.png" style="width: 20px; heigth: 20px" class="m-3" alt="nerd">
                    <p style="display: inline" class="">Nerd</p>
                </div>
                {/each}
            </div>
            <div style="height: 50%; overflow: auto">
                <div class="bg-body rounded" style="width: 100%">
                    {#each n as i}
                        <div class="mb-1" style="width: 100%">
                            <img src="https://em-content.zobj.net/thumbs/320/twitter/322/nerd-face_1f913.png" style="width: 20px; heigth: 20px" class="m-3" alt="nerd">
                            <p style="display: inline" class="">Ahh</p>
                        </div>
                    {/each}
                    <textarea class="form-control" style="height: 20px"></textarea>
                    <button class="form-control btn btn-primary" style="">Enviar</button>
                </div>
            </div>
        </div>
    </div>
</main>

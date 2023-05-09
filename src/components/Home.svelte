<script>
    var n = [1, 1, 1, 1, 1, 1, 1, 1, 1];
</script>

<main>
    <div
        style="height: 100%; width: 75%; position: absolute; top: 0; left: 0;"
        class="p-3"
    >
        <div style="height: 100%" class="shadow-none p-3 bg-light rounded">
            <div style="height: 100%; overflow: auto">
                <!-- class= "hide-scrollbar" para esconder scrollbar -->
                <div class="card mb-3">
                    <div class="card-body">
                        <div class="row">
                            <div class="col-md-1">
                                <!-- This div will take up 10% of the left space -->
                                <div>
                                    <img
                                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                                        style="width: 50px; heigth: 50px"
                                        class="m-1"
                                        alt="user"
                                    />
                                </div>
                            </div>
                            <div class="col-md-11">
                                <!-- The main content of the card-body goes here -->
                                <div class="mb-3">
                                    <textarea
                                        class="form-control"
                                        placeholder="Escrever publicação..."
                                        rows="3"
                                    />
                                </div>
                                <div
                                    class="d-flex justify-content-between align-items-center"
                                >
                                    <div class="d-flex">
                                        <button
                                            type="button"
                                            class="btn btn-link"
                                            ><i
                                                class="bi bi-image-fill"
                                            /></button
                                        >
                                        <button
                                            type="button"
                                            class="btn btn-link"
                                            ><i
                                                class="bi bi-emoji-smile"
                                            /></button
                                        >
                                        <button
                                            type="button"
                                            class="btn btn-link"
                                            ><svg
                                                xmlns="http://www.w3.org/2000/svg"
                                                class="svg-icon"
                                                style="width: 1em; height: 1em;vertical-align: middle;fill: currentColor;overflow: hidden;"
                                                viewBox="0 0 1024 1024"
                                                version="1.1"
                                                ><path
                                                    d="M128 938.666667V341.333333h170.666667v597.333334H128m298.666667 0V85.333333h170.666666v853.333334h-170.666666m298.666666 0v-341.333334h170.666667v341.333334h-170.666667z"
                                                    fill=""
                                                /><path
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    d="M128 938.666667V341.333333h170.666667v597.333334H128m298.666667 0V85.333333h170.666666v853.333334h-170.666666m298.666666 0v-341.333334h170.666667v341.333334h-170.666667z"
                                                    fill=""
                                                /></svg
                                            ></button
                                        >
                                    </div>
                                    <button class="btn btn-primary"
                                        >Publicar</button
                                    >
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                {#each n as i}
                    <div class="p-3 mt-3 bg-body rounded" style="width: 100%">
                        <img
                            src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                            style="width: 50px; heigth: 50px"
                            class="m-3"
                            alt="user"
                        />
                        <h5 style="display: inline" class="">User</h5>
                        <p class="m-3">
                            Lorem ipsum dolor sit amet, consectetur adipiscing
                            elit, sed do eiusmod tempor incididunt ut labore et
                            dolore magna aliqua. Ut enim ad minim veniam, quis
                            nostrud exercitation ullamco laboris nisi ut aliquip
                            ex ea commodo consequat. Duis aute irure dolor in
                            reprehenderit in voluptate velit esse cillum dolore
                            eu fugiat nulla pariatur. Excepteur sint occaecat
                            cupidatat non proident, sunt in culpa qui officia
                            deserunt mollit anim id est laborum.
                        </p>
                        <img
                            src="https://i.kym-cdn.com/entries/icons/original/000/039/761/nerdfacecover.jpg"
                            style="width: 100%"
                            alt="nerd"
                        />
                    </div>
                {/each}
            </div>
        </div>
    </div>
    <div
        style="height: 100%; width: 25%; position: absolute; top: 0; right: 0;"
        class="p-3"
    >
        <div style="height: 100%" class="shadow-none p-3 bg-light rounded">
            <div style="height: 50%; overflow: auto">
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Marco Almeida</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Daniel Silva</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Adalberto Rosário</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Maria Nunes</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">João Rosa</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Ana Mota</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">João Paz</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Luis Azevedo</p>
                </div>
                <div class="mb-1 bg-body rounded" style="width: 100%">
                    <img
                        src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                        style="width: 20px; heigth: 20px"
                        class="m-3"
                        alt="user"
                    />
                    <p style="display: inline" class="">Gustavo Teixeira</p>
                </div>
            </div>
            <div style="height: 50%; overflow: auto">
                <div class="bg-body rounded" style="width: 100%">
                    {#each n as i}
                        <div class="mb-1" style="width: 100%">
                            <img
                                src="https://cdn4.iconfinder.com/data/icons/small-n-flat/24/user-alt-512.png"
                                style="width: 20px; heigth: 20px"
                                class="m-3"
                                alt="user"
                            />
                            <p style="display: inline" class="">Ahh</p>
                        </div>
                    {/each}
                    <textarea class="form-control" style="height: 20px" />
                    <button class="form-control btn btn-primary" style=""
                        >Enviar</button
                    >
                </div>
            </div>
        </div>
    </div>
</main>

<style>
    .hide-scrollbar {
        overflow-y: scroll;
        /* set the height and width of the element as needed */
    }

    .hide-scrollbar::-webkit-scrollbar {
        display: none;
    }
</style>

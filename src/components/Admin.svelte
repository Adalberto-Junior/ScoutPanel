<script>
    import Inscrever from "./Inscrever.svelte";
    import MemberList from "./MemberList.svelte";
    
    import {admin_tab} from '../stores/stores.js'
    let _admin_tab;
	admin_tab.subscribe(value => {
		_admin_tab = value;
	});
</script>

<main>
    <div style="height: 100%; width: 25%; position: absolute; top: 0; left: 0;">
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 text-bg-success rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab.update(()=>"lista")}>Lista de membros</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 text-bg-success rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab.update(()=>"inscrever")}>Inscrever novo membro</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab.update(()=>"pedidos")}>Pedidos de requerimentos</a></div>
        <div class="shadow-none p-3 mt-3 mb-3 mw-3 bg-light rounded"><a href="#" class="nav-link" style="display: block" on:click={()=>admin_tab.update(()=>"estatisticas")}>Estatísticas</a></div>
    </div>
    <div style="height: 100%; width: 75%; position: absolute; top: 0; right: 0;">
        {#if _admin_tab=="inscrever"}
            <div style="height: 95%; overflow: auto">
                <Inscrever/>
            </div>
        {:else if _admin_tab=="lista"}
        <div style="height: 95%; overflow: auto">
            <MemberList/>
        </div>
        {/if}
    </div>
</main>

<script>
 export let content;
 export let activeItem;
</script>
{#each content as item}
{#if item.Time===activeItem}
<div class="tab-body">
<p><span>Type:</span><span class="body-content">{item.Type}</span></p>
<p><span>Item:</span><span class="body-content">{item.Item}</span></p>
<p><span>Quantity:</span><span class="body-content">{item.Quantity}</span></p>
</div>
{/if}
{/each}
<style>
    .tab-body
    {
        width: 70%;
        height:100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin: 1rem 0rem;
    }
    .tab-body p{
        font-size: 1rem;
        font-weight: bold;
        width: 70%;
        display: flex;
    }
    .body-content
    {
        margin-left: .4rem;
    }
</style>
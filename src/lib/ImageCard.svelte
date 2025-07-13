<script>
    export let image;  // Image URL prop
    export let title;  // Title prop
    export let description;  // Description prop
</script>
  
<style>
    .card {
        background-color: #DBFFCB;
        border: 3px solid #BEE4D0;
        border-radius: 10px;
        overflow: hidden;
        width: 270px;
        height: 350px;
        overflow-y: auto;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        margin: 20px;
        text-align: center;
    }
  
    .card img {
        width: 100%;
        height: auto;
        border-radius: 5px;
    }
  
    .card-content {
        padding: 15px;
        background-color: #DBFFCB;
    }
  
    .card-title {
        font-size: 1.5em;
        color: #FF6363;
        font-family: "Quicksand", sans-serif;
        margin: 0 0 10px 0;
        background-color: #DBFFCB;
    }
  
    .card-description {
        font-size: 1em;
        color: #000000;
        font-family: "Quicksand", sans-serif;
        font-weight: 500;
        margin: 0;
        background-color: #DBFFCB;
    }
</style>
  
<div class="card">
    <img src={image} alt={title} />
    <div class="card-content">
      <h2 class="card-title">{title}</h2>
      <p class="card-description">{description}</p>
    </div>
</div>
  
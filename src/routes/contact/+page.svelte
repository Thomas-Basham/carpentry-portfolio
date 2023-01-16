<script>
   let name = "Thomas Basham";
   let phone = "253-258-2526";
   let email = "bashamtg@gmail.com";
   let location = "Renton, Washington";
</script>

<div class="container right-space pt-5">
  <h1 class="text-center">Contact {name}</h1>
  <div class="card">
      <div class="card-body">
          <p class="card-text">Phone: {phone}</p>
          <p class="card-text">Email: <a href="mailto:{email}">{email}</a></p>
          <p class="card-text">Location: {location}</p>
      </div>
  </div>
</div>
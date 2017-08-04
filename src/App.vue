<template>
  <div id="app">
	  <div class="container">
	  	<div style="margin-top: 2rem; padding-bottom: 1rem;"><h1>Make Bootstrap Sexy Again</h1></div>
		<!-- Alerts -->
		<h2>Alerts</h2>
		<div style="padding: 1rem;">
			<div v-for="brand in ['success', 'info', 'warning', 'danger']" class="alert" :class="'alert-' + brand">
	  		  <strong>Well done!</strong> You successfully read this {{brand}} alert message.
	  	    </div>
		</div>
		<h2>Breadcrumb</h2>
		<div style="padding: 1rem;">
			<ol class="breadcrumb">
			  <li class="breadcrumb-item"><a href="#">Home</a></li>
			  <li class="breadcrumb-item"><a href="#">Library</a></li>
			  <li class="breadcrumb-item active">Data</li>
			</ol>
		</div>
		<!-- Badges-->
		<h2>Badges</h2>
		<div style="padding: 1rem;">
		  <span v-for="brand in ['default', 'primary', 'success', 'info', 'warning', 'danger']">
			  <span class="badge" :class="'badge-' + brand" style="margin-right: 0.333rem;">
				  {{brand}}
			  </span>
		  </span>
		</div>
		<!-- Buttons-->
		<h2>Buttons</h2>
		<div style="padding: 1rem;">
			  <div v-for="type in [null, 'outline']">
				  <span v-for="brand in ['primary', 'secondary', 'success', 'info', 'warning', 'danger']">
					  <button role="button" class="btn" :class="'btn-' + (type != null ? (type + '-') : '') + brand" style="margin-bottom: 1rem; margin-right: 1rem;">
						  {{brand}} {{type}}
					  </button>
				  </span>
			  </div>
			  <div class="btn-group" data-toggle="buttons">
			    <label class="btn btn-primary active">
			      <input type="radio" name="options" id="option1" autocomplete="off" checked> Radio 1 (preselected)
			    </label>
			    <label class="btn btn-primary">
			      <input type="radio" name="options" id="option2" autocomplete="off"> Radio 2
			    </label>
			    <label class="btn btn-primary">
			      <input type="radio" name="options" id="option3" autocomplete="off"> Radio 3
			    </label>
			  </div>
		</div>
		<!-- Progress-->
		<h2>Progress</h2>
		<div style="padding: 1rem;">
		  <div v-for="brand in ['success', 'info', 'warning', 'danger']" class="progress" style='margin-bottom: 1rem;'>
			  <div class="progress-bar" :class="'bg-' + brand" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
		  </div>
		</div>
		<!-- Navbar -->
		<h2>Navbar</h2>
		<div style="padding: 1rem;">
			<div v-for="color in ['bg-inverse', 'bg-primary']" style="padding-bottom: 1rem;">
				<nav class="navbar navbar-inverse" :class="color">
					<a class="navbar-brand" href="#">{{color}} navbar</a>
				    <div class="collapse navbar-collapse" id="">
				      <ul class="navbar-nav">
				        <li class="nav-item active">
				          <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
				        </li>
				        <li class="nav-item">
				          <a class="nav-link" href="#">Features</a>
				        </li>
				        <li class="nav-item">
				          <a class="nav-link" href="#">Pricing</a>
				        </li>
				        <li class="nav-item">
				          <a class="nav-link disabled" href="#">Disabled</a>
				        </li>
				      </ul>
				    </div>
				</nav>
			</div>
		</div>
		<!-- Notice-->
		<h2>Modal</h2>
		<div style="padding: 1rem;">
		  <div class="modal-dialog" role="document">
		    <div class="modal-content">
		      <div class="modal-header">
		        <h5 class="modal-title">Modal title</h5>
		        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
		          <span aria-hidden="true">&times;</span>
		        </button>
		      </div>
		      <div class="modal-body">
		        <p>Modal body text goes here.</p>
		      </div>
		      <div class="modal-footer">
		        <button type="button" class="btn btn-primary">Save changes</button>
		        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
		      </div>
		    </div>
		  </div>
		</div>
		<!-- Spacing utilities-->
		<h2>Spacing utilities</h2>
		<div style="padding: 1rem;">
		  <div v-for="brand in ['success', 'info', 'warning', 'danger']" class="progress" style='margin-bottom: 1rem;'>
			  <div class="progress-bar" :class="'bg-' + brand" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
		  </div>
		</div>
	  </div>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
@import "./styles/custom-bootstrap.scss";
@import "../node_modules/bootstrap/scss/bootstrap.scss";
</style>

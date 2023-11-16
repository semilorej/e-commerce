<!-- Import Bootstrap CSS -->
<script>
	// ... (other imports and data)

	// Hero section data
	let heroTitle = 'Welcome to Our Eye Products Store';
	let heroSubtitle = 'Discover a wide range of high-quality eye products.';

	// Testimonials data
	let testimonials = [
		{
			name: 'John Doe',
			review:
				'I love the quality of the eyeglasses I purchased. They are stylish and comfortable to wear.',
			image: 'john_doe.jpg' // Replace with an image URL
		},
		{
			name: 'Jane Smith',
			review:
				'The customer support is outstanding. They helped me choose the perfect contact lenses.',
			image: 'jane_smith.jpg' // Replace with an image URL
		}
		// Add more testimonials here
	];

	// FAQ data
	let faqData = [
		{
			question: 'How do I place an order?',
			answer:
				'You can place an order by selecting the product you want and clicking "Add to Cart." Then, proceed to the checkout process.'
		},
		{
			question: 'What is the return policy?',
			answer:
				'Our return policy allows returns within 30 days of purchase. Please check our Returns and Refunds page for more details.'
		}
		// Add more FAQ questions and answers here
	];

	// Features data
	let features = [
		{
			title: 'Variety of Products',
			description: 'Explore a wide selection of eyeglasses, contact lenses, and more.'
		},
		{
			title: 'Quality Assurance',
			description: 'Our products are sourced from trusted manufacturers to ensure quality.'
		},
		{
			title: 'Customer Support',
			description: 'We provide excellent customer support for all your inquiries.'
		}
	];

	// Pricing plans data
	let pricingPlans = [
		{
			name: 'Eyeglasses',
			price: '$49.99 - $149.99',
			description: 'Stylish and prescription eyeglasses for all occasions.'
		},
		{
			name: 'Contact Lenses',
			price: '$29.99 - $69.99',
			description: 'Comfortable and convenient monthly supply of contact lenses.'
		},
		{
			name: 'Accessories',
			price: '$9.99 - $24.99',
			description: 'Eyeglass cases, cleaning kits, and more accessories.'
		}
	];

	// Contact information
	let contactEmail = 'contact@eyeproductsstore.com';
	let contactPhone = '(123) 456-7890';

	// Product data with high-quality images (replace with actual image URLs)
	let products = [
		{
			id: 1,
			name: 'Classic Black Eyeglasses',
			description: 'Timeless black eyeglasses for a classic look.',
			price: 59.99,
			image: '/classic_black_eyeglasses.jpg' // Replace with a high-quality image URL
		},
		{
			id: 2,
			name: 'Sports Sunglasses',
			description: 'Sunglasses designed for sports enthusiasts.',
			price: 69.99,
			image: '/sports_sunglasses.jpg' // Replace with a high-quality image URL
		},

		{
			id: 3,
			name: 'Retro Round Glasses',
			description: 'Achieve a retro look with these stylish round glasses.',
			price: 49.99,
			image: '/retro_round_glasses.jpg' // Replace with a high-quality image URL
		},
		{
			id: 4,
			name: 'UV Protection Clip-On Sunglasses',
			description: 'Clip-on sunglasses for UV protection with convenience.',
			price: 29.99,
			image: '/uv_protection_clip_on_sunglasses.jpg' // Replace with a high-quality image URL
		},
		{
			id: 5,
			name: 'Reading Glass',
			description: 'Set of reading glasses for various reading needs.',
			price: 44.99,
			image: '/reading_glass.jpg' // Replace with a high-quality image URL
		},
		{
			id: 6,
			name: 'Fashionable Cat Eye Frame',
			description: 'Cat-eye frames for a trendy and fashionable look.',
			price: 79.99,
			image: '/fashionable_cat_eye_frame.jpg' // Replace with a high-quality image URL
		},

		{
			id: 8,
			name: 'Elegant Gold-Trimmed Glasses',
			description: 'Glasses with an elegant touch of gold trimming.',
			price: 89.99,
			image: '/elegant_gold_trimmed_glasses.jpg' // Replace with a high-quality image URL
		},

		{
			id: 10,
			name: 'Designer Eyeglasses 1',
			description: 'High-end designer eyeglasses for a touch of luxury.',
			price: 199.99,
			image: '/designer_eyeglasses1.jpg' // Replace with a high-quality image URL
		},

		{
			id: 14,
			name: 'Fashionable Reading Glasses',
			description:
				'Stay stylish while enhancing your reading experience with fashionable reading glasses.',
			price: 59.99,
			image: '/fashionable_reading_glasses.jpg' // Replace with a high-quality image URL
		}

		// Add more products here
	];
</script>

<section class="hero bg-primary text-white text-center py-5">
	<div class="container">
		<h1 class="display-4">{heroTitle}</h1>
		<p class="lead">{heroSubtitle}</p>
		<a href="#products" class="btn btn-light btn-lg">Explore Products</a>
	</div>
</section>

<section id="products" class="py-5">
	<div class="container">
		<h2 class="text-center">Our Eye Products</h2>
		<div class="row">
			{#each products as product (product.id)}
				<div class="col-md-4">
					<div class="card mb-4">
						<img src={product.image} alt={product.name} class="card-img-top" />
						<div class="card-body">
							<h3 class="card-title">{product.name}</h3>
							<p class="card-text">{product.description}</p>
							<h4 class="card-subtitle">${product.price.toFixed(2)}</h4>
							<button class="btn btn-primary">Add to Cart</button>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-5">
	<div class="container">
		<div class="row">
			{#each features as feature (feature.title)}
				<div class="col-md-4">
					<h2>{feature.title}</h2>
					<p>{feature.description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="bg-light py-5" id="pricing">
	<div class="container">
		<h2 class="text-center">Pricing</h2>
		<div class="row">
			{#each pricingPlans as plan (plan.name)}
				<div class="col-md-4">
					<div class="card mb-4">
						<div class="card-body">
							<h3 class="card-title">{plan.name}</h3>
							<p class="card-text">{plan.description}</p>
							<h4 class="card-subtitle">{plan.price}</h4>
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-5" id="contact">
	<div class="container">
		<h2 class="text-center">Contact Us</h2>
		<div class="row">
			<div class="col-md-6">
				<p>If you have any questions, feel free to contact us:</p>
				<ul>
					<li>Email: {contactEmail}</li>
					<li>Phone: {contactPhone}</li>
				</ul>
			</div>
			<div class="col-md-6">
				<form>
					<div class="form-group">
						<label for="name">Name</label>
						<input type="text" class="form-control" id="name" />
					</div>
					<div class="form-group">
						<label for="email">Email</label>
						<input type="email" class="form-control" id="email" />
					</div>
					<div class="form-group">
						<label for="message">Message</label>
						<textarea class="form-control" id="message" rows="5" />
					</div>
					<button type="submit" class="btn btn-primary">Submit</button>
				</form>
			</div>
		</div>
	</div>
</section>

<section class="bg-light py-5">
	<div class="container">
		<h2 class="text-center">Testimonials</h2>
		<div class="row">
			{#each testimonials as testimonial (testimonial.name)}
				<div class="col-md-6">
					<div class="testimonial">
						<p class="testimonial-text">{testimonial.review}</p>
						<p class="testimonial-author">- {testimonial.name}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<section class="py-5">
	<div class="container">
		<h2 class="text-center">Frequently Asked Questions</h2>
		<div class="accordion" id="faqAccordion">
			{#each faqData as faq (faq.question)}
				<div class="card">
					<div class="card-header" id={'faqHeading' + faq.question}>
						<h5 class="mb-0">
							<button
								class="btn btn-link"
								type="button"
								data-toggle="collapse"
								data-target={'#faqCollapse' + faq.question}
								aria-expanded="true"
								aria-controls={'faqCollapse' + faq.question}
							>
								{faq.question}
							</button>
						</h5>
					</div>
					<div
						id={'faqCollapse' + faq.question}
						class="collapse"
						aria-labelledby={'faqHeading' + faq.question}
						data-parent="#faqAccordion"
					>
						<div class="card-body">
							{faq.answer}
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<footer class="bg-dark text-white text-center py-3">
	<div class="container">
		<p>&copy; 2023 Eye Products Store</p>
	</div>
</footer>

<slot />

<style>
	/* Add background styles */

	/* Style the form elements */
	.form-group {
		margin-bottom: 20px;
	}

	.form-control {
		border: 2px solid #3498db;
		border-radius: 4px;
	}

	.form-control:focus {
		border-color: #007bff;
		box-shadow: none;
	}

	.btn-primary {
		background-color: #007bff;
		border: none;
	}

	.btn-primary:hover {
		background-color: #0056b3;
	}
</style>

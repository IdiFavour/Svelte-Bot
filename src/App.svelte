<script>
	let message = "";
	let messages = [];

	const sendMsg = () => {
		messages = [
			...messages,
			{
				msg: message,
			},
		];

		message = "";
	};
	console.log(message);
	console.log(messages);
</script>

<main class="text-gray-900 leading-tight">
	<div class="min-h-screen bg-gray-100">
		<div
			class="min-h-full flex items-center justify-center py-6 px-4 sm:px-6 lg:px-8"
		>
			<div class="max-w-md w-full space-y-8">
				<div>
					<img
						class="mx-auto h-12 w-auto"
						src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg"
						alt="Workflow"
					/>
					<h2 class="mt-2 text-center text-3xl font-extrabold text-gray-900">
						Svelte Bot
					</h2>
					<p class=" text-center text-sm text-gray-600">
						
						<a href="https://idifavour.netlify.app/" class="font-medium text-indigo-600 hover:text-indigo-500">
						  Created by Idi Favour
						</a>
					  </p>
				</div>
				<div class="container">
					<!-- ... -->
					<!-- This example requires Tailwind CSS v2.0+ -->
					<div class="bg-white shadow overflow-hidden sm:rounded-lg">
						<div class="border-t border-gray-200">
							<div class="flex-1 p:2 sm:p-6 justify-between flex flex-col h-bot ">
								<div class="message-card h-full flex flex-col space-y-2 overflow-y-auto scrollbar-thumb-blue scrollbar-thumb-rounded scrollbar-track-blue-lighter scrollbar-w-2 scrolling-touch"
								>
									{#each messages as me, index}
										<div class="flex items-end overflow:hidden  justify-end"
										>
											<div class="flex flex-col space-y-2 text-xs max-w-xs mx-2 order-1 items-end"
											>
												<div>
													<span
														class="px-4 py-2 rounded-lg inline-block rounded-br-none bg-blue-600 text-white "
													>
														{me.msg}
													</span>
												</div>
											</div>
										</div>
									{:else}
										<p class="text-center">No Chat</p>
									{/each}
									<!-- <div class="flex items-end my-2">
										<div
											class="flex flex-col space-y-2 text-xs max-w-xs mx-2 order-2 items-start"
										>
											<div>
												<span
													class="px-4 py-2 rounded-lg inline-block rounded-bl-none bg-gray-300 text-gray-600"
													>Can be verified on any
													platform using docker</span
												>
											</div>
										</div>
										<img
											src="https://images.unsplash.com/photo-1549078642-b2ba4bda0cdb?ixlib=rb-1.2.1&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=3&amp;w=144&amp;h=144"
											alt="My profile"
											class="w-6 h-6 rounded-full order-1"
										/>
									</div> -->
									
								</div>

								<div
									class="border-t-2 border-gray-200 px-4 pt-4 mb-2 sm:mb-0 object-bottom"
								>
									<div class="relative flex">
										<span
											class="absolute inset-y-0 flex items-center"
										>
											<button
												type="button"
												class="inline-flex items-center justify-center rounded-full h-12 w-12 transition duration-500 ease-in-out text-gray-500 hover:bg-gray-300 focus:outline-none"
											>
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke="currentColor"
													class="h-6 w-6 text-gray-600"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														stroke-width="2"
														d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z"
													/>
												</svg>
											</button>
										</span>
										<input
											type="text"
											bind:value={message}
											placeholder="Write Something"
											class="w-full focus:outline-none focus:placeholder-gray-400 text-gray-600 placeholder-gray-600 pl-12 bg-gray-200 rounded-full py-3"
										/>
										<div
											class="absolute right-0 items-center inset-y-0 hidden sm:flex"
										>
											<button
												type="button"
												class="inline-flex items-center justify-center rounded-full h-10 w-10 transition duration-500 ease-in-out text-gray-500 hover:bg-gray-300 focus:outline-none"
											>
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke="currentColor"
													class="h-6 w-6 text-gray-600"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														stroke-width="2"
														d="M15.172 7l-6.586 6.586a2 2 0 102.828 2.828l6.414-6.586a4 4 0 00-5.656-5.656l-6.415 6.585a6 6 0 108.486 8.486L20.5 13"
													/>
												</svg>
											</button>
											<button
												type="button"
												class="inline-flex items-center justify-center rounded-full h-10 w-10 transition duration-500 ease-in-out text-gray-500 hover:bg-gray-300 focus:outline-none"
											>
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke="currentColor"
													class="h-6 w-6 text-gray-600"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														stroke-width="2"
														d="M3 9a2 2 0 012-2h.93a2 2 0 001.664-.89l.812-1.22A2 2 0 0110.07 4h3.86a2 2 0 011.664.89l.812 1.22A2 2 0 0018.07 7H19a2 2 0 012 2v9a2 2 0 01-2 2H5a2 2 0 01-2-2V9z"
													/>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														stroke-width="2"
														d="M15 13a3 3 0 11-6 0 3 3 0 016 0z"
													/>
												</svg>
											</button>
											<button
												type="button"
												class="inline-flex items-center justify-center rounded-full h-10 w-10 transition duration-500 ease-in-out text-gray-500 hover:bg-gray-300 focus:outline-none"
											>
												<svg
													xmlns="http://www.w3.org/2000/svg"
													fill="none"
													viewBox="0 0 24 24"
													stroke="currentColor"
													class="h-6 w-6 text-gray-600"
												>
													<path
														stroke-linecap="round"
														stroke-linejoin="round"
														stroke-width="2"
														d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
													/>
												</svg>
											</button>
											<button
												type="button"
												on:click={sendMsg}
												class="inline-flex items-center justify-center rounded-full h-12 w-12 transition duration-500 ease-in-out text-white bg-blue-500 hover:bg-blue-400 focus:outline-none"
											>
												<svg
													xmlns="http://www.w3.org/2000/svg"
													viewBox="0 0 20 20"
													fill="currentColor"
													class="h-6 w-6 transform rotate-90"
												>
													<path
														d="M10.894 2.553a1 1 0 00-1.788 0l-7 14a1 1 0 001.169 1.409l5-1.429A1 1 0 009 15.571V11a1 1 0 112 0v4.571a1 1 0 00.725.962l5 1.428a1 1 0 001.17-1.408l-7-14z"
													/>
												</svg>
											</button>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</main>

<style>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

	.container {
		margin-top: 10px !important;
	}

	.h-bot {
		height: 30rem;
	}

	.scrollbar-w-2::-webkit-scrollbar {
		width: 0.25rem;
		height: 0.25rem;
	}

	.scrollbar-track-blue-lighter::-webkit-scrollbar-track {
		--bg-opacity: 1;
		background-color: #f7fafc;
		background-color: rgba(247, 250, 252, var(--bg-opacity));
	}

	.scrollbar-thumb-blue::-webkit-scrollbar-thumb {
		--bg-opacity: 1;
		background-color: #edf2f7;
		background-color: rgba(237, 242, 247, var(--bg-opacity));
	}

	.scrollbar-thumb-rounded::-webkit-scrollbar-thumb {
		border-radius: 0.25rem;
	}
</style>

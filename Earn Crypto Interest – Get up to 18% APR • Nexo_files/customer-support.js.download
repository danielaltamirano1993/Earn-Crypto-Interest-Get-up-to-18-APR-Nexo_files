function initCustomerSupport() {
	const isHelpCenter = window.location.hostname === "sct11.nexo.io";
	const helpButtonLabel = isHelpCenter ? "Live Chat" : "Help";

	function track(category, action) {
		if (window.dataLayer) {
			window.dataLayer.push({
				event: "dynamic_event",
				eventCategory: category,
				eventAction: action,
				eventLabel: "Web Chat"
			});
		}
	}

	const shadowHost = document.createElement("div");
	const shadow = shadowHost.attachShadow({ mode: "open" });
	shadow.innerHTML = `
		<form class="nexo-cs-form js-form">
			<div class="nexo-cs-form__header">
				<span class="nexo-cs-form__header-label">
					Help
				</span>
				<button class="nexo-cs-form__header-button js-form-close" type="button" aria-label="close">
					<svg width="14" height="14" viewBox="0 0 14 14">
						<path d="M8.46792 6.97809L12.9812 2.50861L13.9014 1.58842C14.0329 1.45696 14.0329 1.23787 13.9014 1.0626L12.9374 0.0985915C12.7621 -0.0328638 12.543 -0.0328638 12.4116 0.0985915L7.02191 5.53208L1.58842 0.0985915C1.45696 -0.0328638 1.23787 -0.0328638 1.0626 0.0985915L0.0985915 1.0626C-0.0328638 1.23787 -0.0328638 1.45696 0.0985915 1.58842L5.53208 6.97809L0.0985915 12.4116C-0.0328638 12.543 -0.0328638 12.7621 0.0985915 12.9374L1.0626 13.9014C1.23787 14.0329 1.45696 14.0329 1.58842 13.9014L7.02191 8.46792L11.4914 12.9812L12.4116 13.9014C12.543 14.0329 12.7621 14.0329 12.9374 13.9014L13.9014 12.9374C14.0329 12.7621 14.0329 12.543 13.9014 12.4116L8.46792 6.97809Z" fill="white" />
					</svg>
				</button>
			</div>

			<div class="nexo-cs-form-content">
				<p class="nexo-cs-form-info">
					Please tell us how we can help you. Thank&nbsp;you.
				</p>

				<div class="nexo-cs-field">
					<label class="nexo-cs-label" for="form-name">Name<span>*</span></label>
					<input class="nexo-cs-input" type="text" id="form-name" required>
				</div>
				<div class="nexo-cs-field">
					<label class="nexo-cs-label" for="form-email">Email<span>*</span></label>
					<input class="nexo-cs-input" type="email" id="form-email" required>
				</div>
				<div class="nexo-cs-field">
					<label class="nexo-cs-label" for="form-message">Message<span>*</span></label>
					<textarea class="nexo-cs-input" id="form-message" required></textarea>
				</div>

				<div class="nexo-cs-button-container">
					<button class="nexo-cs-button" id="prechat-form-submit" type="submit">Start Chat</button>
				</div>
			</div>
		</form>

		<button class="nexo-cs-help-button js-form-toggle is-active">
			<svg width="24" height="20" viewBox="0 0 24 20">
				<path d="M19.508 18.5778V14.4617C19.508 13.3134 17.6219 14.4555 15.0334 14.6167C15.0334 17.1213 17.3424 18.4929 18.9132 19.0151C19.2133 19.1148 19.508 18.887 19.508 18.5778Z" fill="white"/>
				<path fill-rule="evenodd" clip-rule="evenodd" d="M8.03119 0.957031C4.03821 0.957031 0.80127 4.19398 0.80127 8.18695C0.80127 12.1799 4.03821 15.4169 8.03119 15.4169H16.0714C20.0643 15.4169 23.3013 12.1799 23.3013 8.18695C23.3013 4.19398 20.0643 0.957031 16.0714 0.957031H8.03119ZM6.77555 9.68701C7.62483 9.68701 8.3133 9.01544 8.3133 8.18701C8.3133 7.35858 7.62483 6.68701 6.77555 6.68701C5.92627 6.68701 5.23779 7.35858 5.23779 8.18701C5.23779 9.01544 5.92627 9.68701 6.77555 9.68701ZM12.0509 9.68701C12.9002 9.68701 13.5887 9.01544 13.5887 8.18701C13.5887 7.35858 12.9002 6.68701 12.0509 6.68701C11.2017 6.68701 10.5132 7.35858 10.5132 8.18701C10.5132 9.01544 11.2017 9.68701 12.0509 9.68701ZM18.8641 8.18701C18.8641 9.01544 18.1756 9.68701 17.3263 9.68701C16.477 9.68701 15.7886 9.01544 15.7886 8.18701C15.7886 7.35858 16.477 6.68701 17.3263 6.68701C18.1756 6.68701 18.8641 7.35858 18.8641 8.18701Z" fill="white"/>
			</svg>
			<span class="nexo-cs-help-button__label">
				${helpButtonLabel}
			</span>
		</button>

		<div class="certainly-button js-sf-toggle maximized">
			<svg viewBox="0 0 16 8" width="32.6" height="14" id="certainly-svg-webchat">
				<title>Open or close chat</title>
				<path d="M16 2.667C16 1.194 14.806 0 13.334 0c-1.473 0-2.667 1.194-2.667 2.667 0 1.472 1.194 2.666 2.667 2.666C14.806 5.333 16 4.14 16 2.667z" fill="#FF0049" id="red-dot-path"></path>
				<path d="M6.333 3.333C5.045 3.333 4 4.378 4 5.667 4 6.955 5.045 8 6.333 8c1.289 0 2.334-1.045 2.334-2.333 0-1.289-1.045-2.334-2.334-2.334z" fill="#FFB769" id="orange-dot-path"></path>
				<path d="M1.333 2.667C.597 2.667 0 3.264 0 4s.597 1.333 1.333 1.333c.737 0 1.334-.597 1.334-1.333S2.07 2.667 1.333 2.667z" fill="#FFC1BE" id="pink-dot-path"></path>
			</svg>
		</div>
	`;

	document.body.appendChild(shadowHost);

	const shadowStyle = document.createElement("style");
	shadowStyle.textContent = `
		@font-face {
			font-family: TT Norms;
			font-weight: 400;
			src: url(https://nexo.io/assets/build/fonts/tt-norms-regular.ttf) format("truetype");
		}

		@font-face {
			font-family: TT Norms;
			font-weight: 500;
			src: url(https://nexo.io/assets/build/fonts/tt-norms-medium.ttf) format("truetype");
		}

		@font-face {
			font-family: TT Norms;
			font-weight: 700;
			src: url(https://nexo.io/assets/build/fonts/tt-norms-bold.ttf) format("truetype");
		}

		button {
			font-family: inherit;
			border: none;
			background: none;
			appearance: none;
			-webkit-appearance: none;

			cursor: pointer;
		}

		.nexo-cs-help-button {
			position: fixed;
			bottom: 10px;
			right: 10px;
			z-index: 1000;

			padding: 10px 16px;
			background-color: #183ead;
			border-radius: 50px;

			font-family: "TT Norms";
			font-weight: bold;
			font-size: 16px;
			line-height: 1.2;
			display: flex;
			align-items: center;
			text-align: center;
			color: #ffffff;

			transition: background-color 0.3s ease, opacity 0.3s ease,
				transform 0.5s cubic-bezier(0.075, 0.82, 0.165, 1);
		}

		@media (max-width: 600px) {
			.nexo-cs-help-button {
				padding: 10px 8px;
			}
		}

		.js-form-toggle:not(.is-active) {
			opacity: 0;
			transform: translateY(50%);
			pointer-events: none;
		}

		.nexo-cs-help-button:hover,
		.nexo-cs-help-button:focus {
			background-color: #122e82;
			outline: none;
		}

		.nexo-cs-help-button:active {
			background-color: #0c1f56;
		}

		.nexo-cs-help-button__label {
			margin-left: 8px;
		}

		@media (max-width: 600px) {
			.nexo-cs-help-button__label {
				display: none;
			}
		}

		.nexo-cs-form {
			position: fixed;
			bottom: 10px;
			right: 10px;
			z-index: 1010;

			max-width: 342px;
			margin: 0;

			font-family: "TT Norms";
			background: #ffffff;
			box-shadow: 0px 8.63767px 40px rgba(5, 7, 52, 0.05);
			border-radius: 8px;
			overflow: hidden;

			transition: opacity 0.3s ease,
				transform 0.5s cubic-bezier(0.075, 0.82, 0.165, 1);
		}

		@media (max-width: 600px) {
			.nexo-cs-form {
				width: 100%;
				max-width: none;
				bottom: 0;
				right: 0;
				border-bottom-left-radius: 0;
				border-bottom-right-radius: 0;
			}

			.nexo-cs-form.is-fullscreen {
				bottom: 0;
				right: 0;
				width: 100%;
				height: 100%;
				max-width: none;
				border-radius: 0;
			}
		}

		.js-form:not(.is-active) {
			opacity: 0;
			transform: translateY(20%);
			pointer-events: none;
		}

		.nexo-cs-form__header {
			position: relative;
			display: flex;
			align-items: center;
			justify-content: center;
			padding: 12px 45px;
			background: #1e4dd8;
		}

		.nexo-cs-form__header-label {
			font-weight: bold;
			font-size: 18px;
			line-height: 1.2;
			color: #ffffff;
		}

		.nexo-cs-form__header-button {
			position: absolute;
			top: 0;
			right: 0;

			display: flex;
			align-items: center;
			justify-content: center;
			width: 45px;
			height: 100%;

			transition: opacity 0.14s ease;
		}

		.nexo-cs-form__header-button:hover,
		.nexo-cs-form__header-button:focus {
			opacity: 0.7;
			outline: none;
		}

		.nexo-cs-form-content {
			padding: 24px;
		}

		.nexo-cs-form-info {
			margin: 0;
			font-weight: 500;
			font-size: 16px;
			line-height: 1.2;
			color: #14171a;
		}

		.nexo-cs-field {
			margin: 16px 0;
		}

		.nexo-cs-label {
			display: block;
			margin-bottom: 4px;
			font-weight: 500;
			font-size: 16px;
			line-height: 1.2;
			color: #4a5056;
		}

		.nexo-cs-label span {
			color: #F03125;
		}

		.nexo-cs-input {
			display: block;
			width: 100%;
			padding: 12px;
			box-sizing: border-box;

			font-family: inherit;
			font-weight: 500;
			font-size: 16px;
			line-height: 1.2;
			color: #14171a;

			background: #ffffff;
			border: 1px solid #e6e9ec;
			border-radius: 4px;

			transition: 0.2s ease;
			resize: none;
			appearance: none;
			-webkit-appearance: none;
		}

		.nexo-cs-input:hover {
			border-color: #1e4dd8;
			outline: none;
		}

		.nexo-cs-input:focus {
			border-color: #122E82;
			outline: none;
		}

		.nexo-cs-button-container {
			display: flex;
			justify-content: flex-end;
		}

		.nexo-cs-button {
			margin-left: auto;
			padding: 10px 16px;
			font-weight: bold;
			font-size: 16px;
			line-height: 1.2;
			background-color: #1e4dd8;
			color: #ffffff;
			border-radius: 4px;
			transition: background-color 0.3s ease;
		}

		.nexo-cs-button:hover,
		.nexo-cs-button:focus {
			background-color: #122e82;
			outline: none;
		}

		.nexo-cs-button:active {
			background-color: #0c1f56;
		}

		.certainly-button {
			position: fixed;
			right: 10px;
			bottom: 10px;
			z-index: 1000;
			display: flex;
			align-items: center;
			justify-content: center;
			width: 56px;
			height: 56px;
			background: #ffffff;
			box-shadow: rgb(0 0 0 / 30%) 0px 1px 4px 0px;
			border-radius: 100px;
			cursor: pointer;
		}

		.certainly-button.maximized {
			background-color: #fff;
		}

		.js-sf-toggle:not(.is-active) {
			display: none;
		}
	`;

	shadow.appendChild(shadowStyle);

	const vendorStyles = document.createElement("style");
	vendorStyles.textContent = `
		:root {
			--certainly-bg-color: #fff;
			--certainly-message-input: #f5f7f9;
			--certainly-chatbot-bubble-background: #331a70;
			--certainly-human-bubble-background: #e5ebee;
			--certainly-chatbot-bubble-text: #fff;
			--certainly-human-bubble-text: #221a39;

			--lwc-sidebarWidth: 400px !important;
			--lwc-colorBrandSecondary: #331a70 !important;
			--lwc-colorBrandSecondaryDarken40: #201048 !important;
			--lwc-colorBrandSecondaryLuminance0: #331a70 !important;
		}

		#botxo-chat-webchat {
			right: 66px !important;
			bottom: 66px !important;
		}

		@media (min-width: 600px) {
			.dockableContainer.showDockableContainer {
				right: 10px !important;
				bottom: 76px !important;
				width: 400px !important;
				box-shadow: 0 1px 4px 0 #00000026 !important;
				border-radius: 8px !important;
			}
		}

		.embeddedServiceLiveAgentStateChatInputFooter .chasitorControls .uiInput {
			padding: 8px !important;
			border: solid 1px #e5ebee !important;
			background-color: #f5f7f9 !important;
			border-radius: 18px !important;
		}

		.embeddedServiceLiveAgentStateChat .messageArea:focus {
			border: none !important;
		}

		.embeddedServiceLiveAgentStateChat .chasitorInputWrapper {
			width: auto !important;
			margin: 18px !important;
			background: none !important;
		}

		.embeddedServiceLiveAgentStateChatInputFooter.dynamicResizeTextOneRow {
			height: 36px !important;
			min-height: 36px !important;
		}

		.embeddedServiceLiveAgentStateChatInputFooter.dynamicResizeTextTwoRows {
			height: 54px !important;
			min-height: 54px !important;
		}

		.embeddedServiceLiveAgentStateChatInputFooter.dynamicResizeTextThreeRows,
		.embeddedServiceLiveAgentStateChatInputFooter.dynamicResizeTextMoreThanThreeRows {
			height: 72px !important;
			min-height: 72px !important;
		}

		.embeddedServiceLiveAgentStateChatInputFooter .chasitorControls {
			height: 100% !important;
			margin: 0 !important;
		}

		embeddedservice-chat-header {
			border-bottom: 1px solid #f3f3f3 !important;
			background: #ffffff !important;
		}

		embeddedservice-chat-header-announcement {
			display: none !important;
		}

		embeddedservice-chat-header h2 {
			visibility: hidden !important;
		}

		embeddedservice-chat-header svg {
			fill: rgb(34, 26, 57) !important;
		}

		embeddedservice-chat-header button {
			padding: 0 8px !important;
		}

		embeddedservice-chat-header .minimizeButton {
			position: relative !important;
			bottom: 2px !important;
		}

		.embeddedServiceSidebarDialogState .dialogButton {
			box-shadow: none !important;
			text-decoration: none !important;
		}
	`;

	document.body.appendChild(vendorStyles);

	const elForm = shadow.querySelector(".js-form");
	const elButton = shadow.querySelector(".js-form-toggle");
	const elFormButton = shadow.querySelector(".js-form-close");
	const elSfButton = shadow.querySelector(".js-sf-toggle");
	const elFormName = shadow.querySelector("#form-name");
	const elFormEmail = shadow.querySelector("#form-email");
	const elFormMessage = shadow.querySelector("#form-message");

	const ua = window.navigator.userAgent.toLowerCase();
	const isExternal = ua.indexOf("nexowallet") >= 0;
	const isFullScreen = window.location.href.indexOf("/customer-support") >= 0;

	let isFormActive = false;
	let isScriptsLoaded = false;
	let isCertainlyActive = true;
	let isSalesforceActive = false;
	let isSfButtonActive = true;
	let isCertainlyInit = false;
	let certainlyConfig = {
		id: "4b983acf-a27d-4a85-8f8c-a499f75898ff",
		mode: "clear_past_conversations",
		webchatKey: "webchat",
		handoverModule: "560552",
		takeoverModule: "560508",
		cvars: {
			visitorName: "John Doe",
			visitorEmail: "jd@email.com"
		}
	};

	if (isFullScreen) {
		shadow.removeChild(elButton);
		elFormButton.parentElement.removeChild(elFormButton);
		elForm.classList.add("is-fullscreen");
		toggleForm();
	} else {
		elButton.addEventListener("click", toggleForm);
		elFormButton.addEventListener("click", toggleForm);
	}

	function toggleForm() {
		if (isExternal && !isFullScreen) {
			window.location.href = "https://nexo.io/customer-support";
			return;
		}

		if (isFormActive) {
			isFormActive = false;
			elForm.classList.remove("is-active");
			elButton.classList.add("is-active");
		} else {
			isFormActive = true;
			elButton.classList.remove("is-active");
			elForm.classList.add("is-active");

			if (window.innerWidth >= 600) {
				elFormName.focus();
			}

			if (!isScriptsLoaded) {
				const certainlyScript = document.createElement("script");
				certainlyScript.src = "https://app.certainly.io/sdk/webchat.js";
				document.body.appendChild(certainlyScript);

				const sfScript = document.createElement("script");
				sfScript.src =
					"https://service.force.com/embeddedservice/5.0/esw.min.js";
				document.body.appendChild(sfScript);

				isScriptsLoaded = true;
			}

			track("Form", "open");
		}
	}

	elSfButton.addEventListener("click", function() {
		if (!isSfButtonActive) {
			// maximize SF chat
			document
				.getElementsByClassName(
					"sidebarHeader minimizedContainer embeddedServiceSidebarMinimizedDefaultUI"
				)[0]
				.click();
		}
	});

	elForm.addEventListener("submit", function(event) {
		event.preventDefault();
		elForm.classList.remove("is-active");

		certainlyConfig.cvars.visitorName = elFormName.value;
		certainlyConfig.cvars.visitorEmail = elFormEmail.value;
		certainlyConfig.cvars.prechatMessage = elFormMessage.value;

		initCertainlyWidget(certainlyConfig, function() {
			if (isCertainlyInit) {
				return;
			}

			certainly.getCertainlyTransfer({
				actionName: certainlyConfig.handoverModule,
				webchatKey: certainlyConfig.webchatKey,
				callback: message => getCertainlyMetadata(message)
			});

			certainly.widgetStatus({
				action: "open", // Required
				webchatKey: certainlyConfig.webchatKey // Required if specified in initCertainlyWidget()
			});

			setTimeout(function() {
				certainly.sendMessage({
					sender: "user", // Required
					message: certainlyConfig.cvars.prechatMessage, // Required
					webchatKey: certainlyConfig.webchatKey // Required if specified in initCertainlyWidget()
				});
			}, 3000);

			isCertainlyInit = true;

			track("Bot Widget", "open");
		});

		track("Form", "submit");
	});

	function getCertainlyMetadata(message) {
		let chatHistory = message && message.cvars ? message.cvars.chatHistory : "";

		embedded_svc.settings.displayHelpButton = false;
		embedded_svc.settings.enabledFeatures = ["LiveAgent"];
		embedded_svc.settings.entryFeature = "LiveAgent";

		embedded_svc.addEventHandler("onChatRequestSuccess", () => {
			// hide salesforce
			var salesforceWidget = document.getElementsByClassName(
				"modalContainer sidebarMaximized layout-docked embeddedServiceSidebar"
			)[0];
			salesforceWidget.style.display = "none";

			var salesforceWidgetButton = document.getElementsByClassName(
				"minimizedContainer embeddedServiceSidebarMinimizedDefaultUI"
			)[0];
			salesforceWidgetButton.style.display = "none";
		});

		embedded_svc.addEventHandler("onChatEstablished", () => {
			elSfButton.classList.add("is-active");
			toggleChatbotVisibility();
			toggleSalesforceVisibility();

			embedded_svc.addEventHandler("afterMinimize", () => {
				toggleSalesforceButton();
			});

			embedded_svc.addEventHandler("afterMaximize", () => {
				toggleSalesforceButton();
			});

			track("Agent Widget", "open");
		});

		embedded_svc.addEventHandler("onChatEndedByChasitor", () => {
			certainlyTakeover();
			track("Agent Widget", "closed by chasitor");
		});

		embedded_svc.addEventHandler("onChatEndedByAgent", () => {
			certainlyTakeover();
			track("Agent Widget", "closed by agent");
		});

		embedded_svc.init(
			"https://nexoio.my.salesforce.com",
			"https://nexosurvey.force.com/support",
			"https://service.force.com",
			"00D2p00000149P9",
			"Nexo_Embedded_Chat",
			{
				baseLiveAgentContentURL:
					"https://c.la1-c2-cdg.salesforceliveagent.com/content",
				deploymentId: "5722p0000008g1z",
				buttonId: "5732p000000Csnv",
				baseLiveAgentURL: "https://d.la1-c2-cdg.salesforceliveagent.com/chat",
				eswLiveAgentDevName:
					"EmbeddedServiceLiveAgent_Parent04I2p000000L0ZvEAK_17a7fad97ab",
				isOfflineSupportEnabled: false
			}
		);

		let interval = setInterval(() => {
			if (embedded_svc.liveAgentAPI) {
				clearInterval(interval);
			} else {
				return;
			}

			embedded_svc.liveAgentAPI.startChat({
				directToAgentRouting: {
					buttonId: "5732p000000Csnv",
					fallback: true
				},
				extraPrechatInfo: [],
				extraPrechatFormDetails: [
					{
						label: "Hello",
						value: chatHistory
							.replace(/\n/g, "<br />")
							.replace(/\[Bot\]/g, "<b>[Bot]</b>")
							.replace(/\[Human\]/g, "<b>[Human]</b>"),
						transcriptFields: ["Certainly_Transcript__c"]
					},
					{
						label: "Provided Name",
						value: certainlyConfig.cvars.visitorName,
						displayToAgent: true,
						transcriptFields: ["Provided_Name__c"]
					},
					{
						label: "Email",
						value: certainlyConfig.cvars.visitorEmail,
						displayToAgent: true,
						transcriptFields: ["Provided_Email__c"]
					},
					{
						label: "issue",
						value: certainlyConfig.cvars.prechatMessage,
						displayToAgent: true,
						transcriptFields: ["Initial_Message__c"]
					}
				]
			});

			window.localStorage.setItem("activeWidget", "SalesForce");
		}, 100);

		track("Bot Widget", "request agent");
	}

	function toggleChatbotVisibility() {
		var certainlyWidget = document.getElementById(
			"botxo-wrapper-" + certainlyConfig.webchatKey
		);
		if (isCertainlyActive) {
			isCertainlyActive = false;
			certainlyWidget.style.display = "none";
		} else {
			isCertainlyActive = true;
			certainlyWidget.style.display = "block";
		}
	}

	function toggleSalesforceVisibility() {
		var salesforceWidget = document.getElementsByClassName(
			"modalContainer sidebarMaximized layout-docked embeddedServiceSidebar"
		)[0];
		if (isSalesforceActive) {
			isSalesforceActive = false;
			salesforceWidget.style.display = "none";
		} else {
			isSalesforceActive = true;
			salesforceWidget.style.display = "block";
		}
	}

	function certainlyTakeover() {
		certainly.goTo(
			{
				module: certainlyConfig.takeoverModule, // Required
				webchatKey: certainlyConfig.webchatKey
			},
			toggleChatbotVisibility //Function (optional)
		);

		embedded_svc.liveAgentAPI.endChat();

		// remove SF chat
		document
			.getElementsByClassName("embeddedServiceSidebar modalContainer")[0]
			.remove();
	}

	function toggleSalesforceButton() {
		if (isSfButtonActive) {
			isSfButtonActive = false;
			elSfButton.classList.remove("maximized");
		} else {
			isSfButtonActive = true;
			elSfButton.classList.add("maximized");
		}
	}
}

// Wait for the <body> to load before appending to it, in case the script is
// included in the <head>.
window.addEventListener("DOMContentLoaded", () => {
	initCustomerSupport();
});

SYSTEM INSTRUCTION PROMPT: High-Fidelity Styling Upgrade & .webp Asset Mapping

You are an expert frontend engineer and a master UI/UX designer. We need to upgrade our current fashion application to look incredibly modern, professional, and visually premium. You must maintain our current color palette but elevate the structural design, typography, cards, and image mapping.

---

### SPECIFICATION 1: EXACT .WEBP ASSET MAPPING
We have placed exactly 8 premium image assets per category into our folder structure. All of these files utilize the `.webp` extension. Update our product mock data arrays/mappings to loop through exactly 8 items per page using the following exact naming conventions:

1. SKIRTS PAGE: Map the items to reference local assets named 'skirt1.webp', 'skirt2.webp', ..., up to 'skirt8.webp'.
2. TOPS PAGE: Map the items to reference local assets named 'top1.webp', 'top2.webp', ..., up to 'top8.webp'.
3. JEWELRY PAGE: Map the items to reference local assets named 'j1.webp', 'j2.webp', ..., up to 'j8.webp'.
4. PANTS PAGE: Map the items to reference local assets named 'pant1.webp', 'pant2.webp', ..., up to 'pant8.webp'.

Each rendered card must seamlessly display the target image alongside its respective title, clear item description text, and a crisp, bold price tag.

---

### SPECIFICATION 2: PREMIUM EDITORIAL HERO & VISUAL STYLING
The current interface is too raw. While preserving our core application colors, implement modern e-commerce visual patterns to elevate the user experience:

1. HERO BACKGROUND INTEGRATION:
   - Integrate our main background fashion photograph, which is saved in the directory as 'image.webp'.
   - Position this as a full-bleed or premium hero background banner at the top of the dashboard workspace to instantly establish a professional, high-end retail look.
   - Apply a soft, elegant linear-gradient overlay (e.g., using subtle black/slate or white/purple gradients depending on the section background) on top of 'image.webp' to ensure text headers, call-to-actions, and navigation components remain perfectly legible and crisp.

2. CARD & CONTAINER REFINEMENT:
   - Structure the product display into a highly responsive CSS Grid (1 column on mobile, 2 on tablet, 4 on desktop) so that it looks stunning across all viewport sizes.
   - Style the product containers with minimalist thin borders, subtle padding rules, and extremely soft micro-shadows.
   - Add smooth, high-fidelity interaction states: when hovering over a product card, implement a subtle image scale-up or an elegant opacity shift to make the browsing experience feel premium and fluid.

3. EDITORIAL TYPOGRAPHY:
   - Clean up font weights and scaling. Use bold, sharp layout treatments for prices and titles, paired with lighter, tracked-out font variations for small labels and item descriptions to create a professional visual hierarchy.

---

Implement these updates across the workspace systematically. Begin by updating the image string arrays to correctly pull the `.webp` assets, then refactor the layout components to introduce the new 'image.webp' hero structure and polished card aesthetics. Provide complete, untruncated, production-grade source files.
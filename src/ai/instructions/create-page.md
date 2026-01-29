# Create Page Instructions

Follow these steps when creating a new page in the application:

1. **Create Route Name Inside Page**
   - Create the appropriate file or directory structure in `src/pages/` to define the route.

2. **Add Page Layout for Astro Template**
   - Apply the standard page layout to the Astro file to ensure consistent styling and structure.
   - For creating user routes, use `src/layouts/PageLayout.astro`.
   - For Moderator routes, use `src/layouts/ModLayout.astro`.

3. **Add Route Components Inside Component/Routes Folder**
   - Create a folder in `src/components/routes/` with the same name as the route.
   - Place all page-specific components inside this new folder.
   - **Client-side Layout**: Use `src/components/routes/@shared/layouts/index.tsx` for client-side pages.
   - **Naming Convention**: Create the page component file named `route.page.tsx` and the component itself should be named using the pattern `RoutePage` (e.g., for a 'login' route, the file is `login.page.tsx` and component is `LoginPage`).
   - **Auto-Layout Wrapping**: If a file with "layout" in its name exists within the folder, all page components in that folder must be wrapped with that layout.

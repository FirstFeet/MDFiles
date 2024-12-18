File Structure
    Package.json
    Package.lock.json
    tailwind.config.js
    postcss.config.mjs - tailwind to normal css package
    next.config.js - Alteration on next js application
    jsconfig.json - Import area configured
    App folder - App related files
Types of component in next App folder
    page.js => Create a new page (e.g., app/about/page.js creates a <your-domain>/about page)
    layout.js => Create a new layout that wraps sibling and nested pages
    not-found.js => Fallback page for "Not Found" errors (thrown by sibling or nested pages or layouts)
    error.js => Fallback page for other errors (thrown by sibling pages or nested pages or layouts)
    loading.js => Fallback page which is shown whilst sibling or nested pages (or layouts) are fetching data
    route.js => Allows you to create an API route (i.e., a page which does NOT return JSX code but instead data, e.g., in the JSON format)
    Template.jsx =>  this is simila r to layout.jsx but  this file reloads all the state of the child components where is the layout file preserves the state  of the child components
    default.js => In a parallel routes If any of the route has inner route then all the parallel route elements should have the same inside them. So to prevent we do a default.js file which will handle of other routes.
npm commands
    npm run dev
    npm run build
    npm run start
Programaticly navigating
    NotFound()
    Redirect()
Improving Accessibility

Component hierachy
    Layout
    Template
    Error
    Loading
    Not-found
    Page
Routing
    Nested Route - route inside folder
    Dynamic routes - []
    Link component navigation - <Link>
    Nested Dynamic routes - Dynamic route inside folder
    Catch all Segments - [[... paramName]]
    Not Found page - not-found.jsx
    File Colocation - 
    Private folders - _folderName
    Route Groups - (routeName) - Just used in folder and will not reflect in the URL path
    parallel routes - @foldername
    route inside Parallel route - using of default.js to prevent not found
    Unmatched routes - Route inside a Parallel route which will render only on code navigation but on page reload it will show page not found
    Conditional routes - Based on condition written on a parallel route different components  can be rendered
    Intercepting routes - (.)folderName - For the same path Different pages are shown depending on where it is redirected. 
    Parallel Intercepting routes - This can be used Image pop up and on refresh we will redirect to new page
    Thorwing Route related errors - error.js
Diff between APP Router and Page Router
Route handlers
    Handling GET
    Handling POST
    Dynamic route handlers
    Handling PATCH
    Handling DELETE
Layouts
    Nested Layouts
    Route group layout
RevalidatePath
Rendering
    CSR
    SSR
    SUSPENSE FOR SSR
    RSC
    server and client components - Server components works only on server side whereas client component works on both server and client side
    RSC rendering life cycle
    Static rendering
        Faster Websites
        Reduced Server Load 
        SEO
    Prefetching in static rendering
    Dynamic rendering
        Real-Time Data 
        User-Specific Content
        Request Time Information
    Streaming
        loading.tsx and Suspense.
        route groups
        loading skeletons
        This can also achieved by parallel routes
    PPR - Partial pre-rendering
        ppr: 'incremental' - in next.config.mjs
        export const experimental_ppr = true; - in the file where PPR has to be implemented
API Communication
    tanstack
    useSWR
    fetch
Query params and path param
    useSearchParams
    usePathname
    useRouter
    Debouncing - import { useDebouncedCallback } from 'use-debounce';
Mutating Data
    Server Action
        With forms
            From server component
            From client component
            Passing as props
        Without froms
            Event Handlers
            UseEffect
    FormData
    useFormState
    React-Email component
    revalidatePath
    revalidateTag
State Management
    Redux, 
    Zustand - https://ijlalwindhi.medium.com/zustand-in-next-js-14-49af1c170d11
    TanStack Query or React Query
URL Query parameter
Redirects in Route handlers
Headers in Route Handlers
Cookies in Route handlers
Metadata
    Routing metadata
    Title metadata
    Static metadata
    Dynamic Metadata
Auth
    Clerk auth
    Next auth
    Passport
    IronSession
Navigating 
    programatically
    using anchor
    using Link
    Active links - usePathName
HttpException
Error handling
Reset function in error boundary
Caching in Route handlers
    cache: 'no-store'
    dynamic = 'force-dynamic'
    { revalidate: 3600, tags: ['posts'] }
    revalidatePath("path")
    
Middleware in next js
    Redirect and rewrite
    Matcher
root file
    Icon png in root
    global.css
@ in import refer to root
Next Image
    render as webp
    priority property
    Fill Property
Next.js's serverless functions API
Next image Slide Show - Carousel
Tailwind
    import clsx from 'clsx' - for conditional style rendering
optimizing-fonts-images
    add custom fonts with next/font
    add images with next/image
    Cumulative Layout Shift
    Height and width in Image
Next Form
    useActionState()
    useFormState - action,InitialValue as Param and return [state, FormAction]
    useFormStatus
AWS S3 with Next JS
i18n
    next-translate
    lingui
    i18next
    react-intl
Other Npm Packages
    Zod - for validation
    react-slick - for react carousel - https://react-slick.neostack.com/
SEO
    next-seo
Next Performance
Next Testing
    Zest
Next deployment
    Next Production build


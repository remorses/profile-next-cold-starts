<div align='center'>
    <br/>
    <br/>
    <br/>
    <h3>Bringing Next.js cold start profiling to the masses</h3>
    <br/>
    <br/>
</div>

## Usage

Add a `vercel.json` in your app directory with the following contents:

```json
{
    "builds": [
        {
            "src": "package.json",
            "use": "https://debug-next-cold-starts.vercel.app/builder.tgz"
        }
    ]
}
```

After you deploy your application, you can append `?vercel-profile-cpu` to an url to download the cpu profile and `?vercel-profile-require` to download a profile of all`require` calls (which is usually what causes long cold starts)

After you download the profile, you can use [trace.cafe](https://trace.cafe) to analyze it or you can also use the VSCode built in visualizer, simply opening the file in VSCode.

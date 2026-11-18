# Scala project template for Yukibana

A starting point for a Yukibana course project in Scala 3 with sbt.

1. On your project's page in Yukibana Cloud, choose **Create from the Scala
   template**, or press **Use this template** above. Then link the new
   repository to the project on the project page.
2. Write the assignment in `ASSIGNMENT.md` and the starting code in `src/`.
   `yukibana.json` says what students see, which files are read-only
   (`readOnly`) and which are left out of the starter (`hidden`, for example
   tests you grade with).
3. Push a tag to publish it to every project linked to this repository:

   ```bash
   git tag v1 && git push origin v1
   ```

   The workflow in `.github/workflows/publish.yml` builds the starter and the
   teacher archive with the Yukibana CLI on GitHub's runners and publishes
   them. It needs no secret: it proves which repository it runs in with
   GitHub's OIDC token (`permissions: id-token: write`). To publish a tag
   again, run the workflow by hand from the Actions tab and pick the tag under
   "Use workflow from": a link publishes only from refs matching its pattern
   (`refs/tags/v*` unless you changed it), so a run from `main` is refused.

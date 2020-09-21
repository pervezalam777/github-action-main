# github-action-main

```yml
      - name: clone another repo
        uses: actions/checkout@v2
        with:
          repository: pervezalam777/webhook-connect-one
          path: webhook-connect-one

      - name: copy file
        run: cp -r ./public ./webhook-connect-one/public

      - name: create translation branch
        run: |
          cd webhook-connect-one
          /usr/bin/git checkout -b translation
      - name: copy translations file
        run: cp -r ./public ./webhook-connect-one/public
      - name: commit and push changes in webhook-connect-one
        run: |
          cd webhook-connect-one
          /usr/bin/git config --global user.email "pervezalam777@gmail.com"
          /usr/bin/git config --global user.name "pervezalam777"
          /usr/bin/git add .
          /usr/bin/git commit -m "translations added"
          /usr/bin/git push --set-upstream origin translation
```
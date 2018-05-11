npm add -D lerna@next

npx lerna init --independent


sed -i -- 's/{{NAME}}/sodium/g' packages/sodium/package.json 

npx lerna bootstrap --hoist  

npx lerna publish --skip-npm --conventional-commits

npx lerna publish --skip-npm --conventional-commits --force-publish

npx lerna add --dev mocha
npx lerna add --dev assert
npx lerna exec --scope=@vdzundza/sodium npm test
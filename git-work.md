| **Step** | **Purpose**                                | **Command** (with your paths & names)                       | **Example Output / Result**        |
| -------- | ------------------------------------------ | ----------------------------------------------------------- | ---------------------------------- |
| 1        | Go to your BYTEXL repo                     | `cd /Users/aspparmar/Desktop/BYTEXL`                        | Terminal switches to BYTEXL folder |
| 2        | Remove old submodule reference (if exists) | `git submodule deinit -f lpu-dsa-II`                        | Removes submodule config           |
| 3        | Remove submodule entry from index          | `git rm -f lpu-dsa-II`                                      | Deletes tracked submodule record   |
| 4        | Remove leftover metadata                   | `rm -rf .git/modules/lpu-dsa-II`                            | Clean internal git storage         |
| 5        | Create fresh folder                        | `mkdir lpu-dsa-II`                                          | Creates empty folder inside BYTEXL |
| 6        | Add a test file (example)                  | `echo "Binary Tree Notes" > lpu-dsa-II/binary-tree.txt`     | Creates file inside folder         |
| 7        | Stage changes                              | `git add .`                                                 | Marks folder + file for commit     |
| 8        | Commit changes                             | `git commit -m "Added lpu-dsa-II folder and initial files"` | Creates commit on `main`           |
| 9        | Push + set upstream                        | `git push -u origin main`                                   | Uploads to GitHub                  |

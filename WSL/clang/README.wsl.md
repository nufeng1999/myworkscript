###从 VSCode 编译 WSL 环境中 C 语言项目使用到的脚本文件
    这些脚本用于 VSCode 运行任务(tasks.json)的配置，目的是使用 Windows 版本的 VSCode 构建调试 WSL 环境中 C 语言项目
#### tasks.json(当 terminal.integrated.shell.windows 为 WSL.EXE时)
    task.json 的内容例子
    {
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Autoscan for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccautoscan",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Aclocal for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccaclocal",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Autoconf for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccautoconf",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Automake for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccautomake",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Configure for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccconfigure",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Clean for Make in WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccprjclean",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Make for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                },
                "cwd":"${workspaceRoot}"
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccmake",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Make install for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccmakeinstall",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Make & Run for WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccmakerun",
            "args": [
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Init autoset for Makefile in WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccmakeinit",
            "args": [
                "\"/mnt/h/myworkscript/WSL/clang\"",
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        },
        {
            "label": "Reinit autoset for Makefile in WSL",
            "type": "shell",
            "options": {
                "env": {
                    "PATH": "$PATH"
                }
            },
            "command": "/mnt/h/myworkscript/WSL/clang/gccmakereinit",
            "args": [
                "\"/mnt/h/myworkscript/WSL/clang\"",
                "\"${workspaceRoot}\""
            ],
            "problemMatcher": {
                "owner": "D",
                "pattern": {
                    "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
                    "file": 1,
                    "line": 2,
                    "column": 3,
                    "severity": 4,
                    "message": 5
                }
            }
        }

    ]
}
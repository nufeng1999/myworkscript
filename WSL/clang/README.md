###从 MSYS2 启动 VSCode 编译 WSL 环境中 C 语言项目使用到的脚本文件
    这些脚本用于从 MSYS2 启动 VSCode 后，运行任务(tasks.json)的配置，目的是使用 Windows 版本的 VSCode 构建调试 WSL 环境中 C 语言项目
#### tasks.json(当 terminal.integrated.shell.windows 为msys64里的base.exe时)
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccautoscan\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccaclocal\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccautoconf\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccautomake\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccconfigure\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
                }
            },
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccmake\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccmakeinstall\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccmakerun\\\"  \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccmakeinit\\\" \\\"/mnt/h/myworkscript/WSL/clang\\\" \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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
            "command": "cmd.exe",
            "args": [
                "/c",
                "\" `cygpath -w /h/myworkscript/Mingw/clang/wslcmdgcc.bat` \\\"/mnt/h/myworkscript/WSL/clang/gccmakereinit\\\" \\\"/mnt/h/myworkscript/WSL/clang\\\" \\\"${workspaceRoot}\\\"  \\\"\\\" \\\"\\\" \""
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

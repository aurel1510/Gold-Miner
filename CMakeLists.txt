cmake_minimum_required(VERSION 3.14)
project(GoldMiner)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add executable
add_executable(GoldMiner
    Animation.cpp
    AnimationSettings.cpp
    Barrel.cpp
    Board.cpp
    BoardObject.cpp
    BoardSettings.cpp
    Button.cpp
    ButtonsSettings.cpp
    Clock.cpp
    ComputerPlayer.cpp
    ContinueButton.cpp
    Controller.cpp
    ControllerSettings.cpp
    DiamondRock.cpp
    Dynamite.cpp
    DynamiteIndicator.cpp
    ExitButton.cpp
    Factory.cpp
    GameController.cpp
    GameOverMenu.cpp
    GoldenRock.cpp
    HomeButton.cpp
    HomeMenu.cpp
    Hook.cpp
    HookSettings.cpp
    HumanPlayer.cpp
    LevelController.cpp
    LevelIndicator.cpp
    LevelSettings.cpp
    Main.cpp
    Menu.cpp
    MultiPlayerBtn.cpp
    MuteButton.cpp
    Object.cpp
    PauseButton.cpp
    PauseMenu.cpp
    Player.cpp
    PlayerSettings.cpp
    RegularRock.cpp
    ResumeButton.cpp
    Rock.cpp
    Score.cpp
    SinglePlayerBtn.cpp
    Sounds.cpp
    SummaryMenu.cpp
    SurpriseBag.cpp
    Textures.cpp
    ToolBar.cpp
    VisualObject.cpp
    VisualObjectSettings.cpp
)

# Find SFML
find_package(SFML 2.5 COMPONENTS graphics window system audio REQUIRED)

# Link SFML libraries
target_link_libraries(GoldMiner
    sfml-graphics
    sfml-window
    sfml-system
    sfml-audio
)

# Include SFML headers
target_include_directories(GoldMiner PRIVATE ${SFML_INCLUDE_DIRS})

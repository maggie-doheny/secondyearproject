/*************************** 
 * Dictatingdecisions *
 ***************************/

import { core, data, sound, util, visual, hardware } from './lib/psychojs-2023.2.3.js';
const { PsychoJS } = core;
const { TrialHandler, MultiStairHandler } = data;
const { Scheduler } = util;
//some handy aliases as in the psychopy scripts;
const { abs, sin, cos, PI: pi, sqrt } = Math;
const { round } = util;


// store info about the experiment session:
let expName = 'dictatingdecisions';  // from the Builder filename that created this script
let expInfo = {
    'participant': `${util.pad(Number.parseFloat(util.randint(0, 999999)).toFixed(0), 6)}`,
    'session': '001',
};

// Start code blocks for 'Before Experiment'
// init psychoJS:
const psychoJS = new PsychoJS({
  debug: true
});

// open window:
psychoJS.openWindow({
  fullscr: true,
  color: new util.Color([0,0,0]),
  units: 'height',
  waitBlanking: true,
  backgroundImage: '',
  backgroundFit: 'none',
});
// schedule the experiment:
psychoJS.schedule(psychoJS.gui.DlgFromDict({
  dictionary: expInfo,
  title: expName
}));

const flowScheduler = new Scheduler(psychoJS);
const dialogCancelScheduler = new Scheduler(psychoJS);
psychoJS.scheduleCondition(function() { return (psychoJS.gui.dialogComponent.button === 'OK'); }, flowScheduler, dialogCancelScheduler);

// flowScheduler gets run if the participants presses OK
flowScheduler.add(updateInfo); // add timeStamp
flowScheduler.add(experimentInit);
flowScheduler.add(WelcomeRoutineBegin());
flowScheduler.add(WelcomeRoutineEachFrame());
flowScheduler.add(WelcomeRoutineEnd());
flowScheduler.add(Welcome_2RoutineBegin());
flowScheduler.add(Welcome_2RoutineEachFrame());
flowScheduler.add(Welcome_2RoutineEnd());
flowScheduler.add(instructions1RoutineBegin());
flowScheduler.add(instructions1RoutineEachFrame());
flowScheduler.add(instructions1RoutineEnd());
flowScheduler.add(practice_decisionRoutineBegin());
flowScheduler.add(practice_decisionRoutineEachFrame());
flowScheduler.add(practice_decisionRoutineEnd());
flowScheduler.add(instructions2RoutineBegin());
flowScheduler.add(instructions2RoutineEachFrame());
flowScheduler.add(instructions2RoutineEnd());
flowScheduler.add(sound_2RoutineBegin());
flowScheduler.add(sound_2RoutineEachFrame());
flowScheduler.add(sound_2RoutineEnd());
flowScheduler.add(instructions2_3RoutineBegin());
flowScheduler.add(instructions2_3RoutineEachFrame());
flowScheduler.add(instructions2_3RoutineEnd());
const trialsLoopScheduler = new Scheduler(psychoJS);
flowScheduler.add(trialsLoopBegin(trialsLoopScheduler));
flowScheduler.add(trialsLoopScheduler);
flowScheduler.add(trialsLoopEnd);















flowScheduler.add(EndRoutineBegin());
flowScheduler.add(EndRoutineEachFrame());
flowScheduler.add(EndRoutineEnd());
flowScheduler.add(quitPsychoJS, '', true);

// quit if user presses Cancel in dialog box:
dialogCancelScheduler.add(quitPsychoJS, '', false);

psychoJS.start({
  expName: expName,
  expInfo: expInfo,
  resources: [
    // resources:
  ]
});

psychoJS.experimentLogger.setLevel(core.Logger.ServerLevel.EXP);


var currentLoop;
var frameDur;
async function updateInfo() {
  currentLoop = psychoJS.experiment;  // right now there are no loops
  expInfo['date'] = util.MonotonicClock.getDateStr();  // add a simple timestamp
  expInfo['expName'] = expName;
  expInfo['psychopyVersion'] = '2023.2.3';
  expInfo['OS'] = window.navigator.platform;


  // store frame rate of monitor if we can measure it successfully
  expInfo['frameRate'] = psychoJS.window.getActualFrameRate();
  if (typeof expInfo['frameRate'] !== 'undefined')
    frameDur = 1.0 / Math.round(expInfo['frameRate']);
  else
    frameDur = 1.0 / 60.0; // couldn't get a reliable measure so guess

  // add info from the URL:
  util.addInfoFromUrl(expInfo);
  

  
  psychoJS.experiment.dataFileName = (("." + "/") + `data/${expInfo["participant"]}_${expName}_${expInfo["date"]}`);
  psychoJS.experiment.field_separator = '\t';


  return Scheduler.Event.NEXT;
}


var WelcomeClock;
var text_10;
var key_resp_3;
var Welcome_2Clock;
var text_71;
var key_resp_6;
var instructions1Clock;
var text_29;
var key_resp_13;
var practice_decisionClock;
var text_30;
var slider_12;
var polygon_2;
var text_8;
var mouse_2;
var instructions2Clock;
var text_34;
var key_resp_16;
var sound_2Clock;
var text;
var sound_3;
var instructions2_3Clock;
var text_49;
var key_resp_31;
var begin_roundClock;
var polygon_9;
var text_47;
var text_70;
var key_resp_40;
var Wait_2Clock;
var text_9;
var key_resp_29;
var DecisionClock;
var text_2;
var slider;
var polygon_10;
var text_7;
var mouse;
var decisionmadeClock;
var text_50;
var sound_1;
var QuestionsClock;
var text_11;
var key_resp_5;
var confidentClock;
var text_12;
var slider_2;
var polygon_4;
var text_16;
var mouse_4;
var polygon;
var text_3;
var guiltyClock;
var text_13;
var slider_3;
var polygon_5;
var text_17;
var mouse_5;
var polygon_3;
var text_5;
var endsmeansClock;
var text_14;
var slider_4;
var polygon_6;
var text_18;
var mouse_6;
var polygon_7;
var text_6;
var rolereversalClock;
var text_15;
var slider_5;
var polygon_8;
var text_19;
var mouse_7;
var polygon_11;
var text_20;
var feelClock;
var text_21;
var slider_6;
var polygon_12;
var text_22;
var mouse_8;
var polygon_13;
var text_23;
var questions_physClock;
var text_58;
var key_resp_7;
var look2Clock;
var text_28;
var slider_7;
var polygon_15;
var text_31;
var mouse_9;
var polygon_16;
var text_32;
var text_33;
var text_35;
var trustClock;
var text_52;
var slider_8;
var polygon_17;
var text_53;
var mouse_10;
var polygon_18;
var text_54;
var text_55;
var text_56;
var endofroundClock;
var text_51;
var sound_4;
var EndClock;
var text_4;
var key_resp_2;
var globalClock;
var routineTimer;
async function experimentInit() {
  // Initialize components for Routine "Welcome"
  WelcomeClock = new util.Clock();
  text_10 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_10',
    text: 'Click spacebar to initialize experiment.',
    font: 'Open Sans',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_3 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "Welcome_2"
  Welcome_2Clock = new util.Clock();
  text_71 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_71',
    text: 'Welcome! Click SPACEBAR to begin when the researcher instructs you to do so.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_6 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "instructions1"
  instructions1Clock = new util.Clock();
  text_29 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_29',
    text: 'PRACTICE TRIAL:\nHere, you will practice choosing your offer amount. Note that the amount you choose is what is given to the receiver. The range of possible offers is $0 to $10. Remember, the amount you select will be given to the receiver, and whatever is leftover  is kept for yourself.\n\nPress SPACEBAR to begin the practice trial.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.1], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_13 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "practice_decision"
  practice_decisionClock = new util.Clock();
  text_30 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_30',
    text: 'Please click the amount that you would like to split with your partner. The amount you click will be given to the receiver for their bonus, and whatever is leftover out of $10 is kept for yourself, and determines the value of your bonus.\n\nClick continue to submit your offer.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.25], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_12 = new visual.Slider({
    win: psychoJS.window, name: 'slider_12',
    startValue: undefined,
    size: [1.3, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["$0", "$1", "$2", "$3", "$4", "$5", "$6", "$7", "$8", "$9", "$10"], fontSize: 0.05, ticks: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_2 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_2', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_8 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_8',
    text: 'CONTINUE',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('black'),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_2 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_2.mouseClock = new util.Clock();
  // Initialize components for Routine "instructions2"
  instructions2Clock = new util.Clock();
  text_34 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_34',
    text: 'Great job! Any questions?\n\nNote that a sound will occur when you submit your decision, and when the round is complete.\n\nClick SPACEBAR to continue and practice hearing the sound.\n',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_16 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "sound_2"
  sound_2Clock = new util.Clock();
  text = new visual.TextStim({
    win: psychoJS.window,
    name: 'text',
    text: 'This is what it will sound like when you submit your decision and when the round concludes.\n',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  sound_3 = new sound.Sound({
      win: psychoJS.window,
      value: 'A',
      secs: 1.0,
      });
  sound_3.setVolume(1.0);
  // Initialize components for Routine "instructions2_3"
  instructions2_3Clock = new util.Clock();
  text_49 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_49',
    text: 'Press SPACEBAR to begin the experiment.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_31 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "begin_round"
  begin_roundClock = new util.Clock();
  polygon_9 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_9', 
    width: [0.25, 0.15][0], height: [0.25, 0.15][1],
    ori: 0.0, pos: [0, 0.33],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([1.0, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: 0, interpolate: true,
  });
  
  text_47 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_47',
    text: 'The researcher will initiate the beginning of this trial.\n\n\n',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: -1.0 
  });
  
  text_70 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_70',
    text: 'WAIT!',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.33], height: 0.07,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -3.0 
  });
  
  key_resp_40 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "Wait_2"
  Wait_2Clock = new util.Clock();
  text_9 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_9',
    text: 'Click SPACEBAR to continue and choose your offer.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_29 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "Decision"
  DecisionClock = new util.Clock();
  text_2 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_2',
    text: 'Please click the amount that you would like to split with your partner.\nThe amount you click will be given to the receiver, and whatever is leftover out of $10 is kept for yourself, and determines the value of your potential giftcard.\n\nClick continue when you have made your decision.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.25], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider = new visual.Slider({
    win: psychoJS.window, name: 'slider',
    startValue: undefined,
    size: [1.3, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["$0", "$1", "$2", "$3", "$4", "$5", "$6", "$7", "$8", "$9", "$10"], fontSize: 0.05, ticks: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_10 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_10', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -3, interpolate: true,
  });
  
  text_7 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_7',
    text: 'CONTINUE',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('black'),  opacity: undefined,
    depth: -4.0 
  });
  
  mouse = new core.Mouse({
    win: psychoJS.window,
  });
  mouse.mouseClock = new util.Clock();
  // Initialize components for Routine "decisionmade"
  decisionmadeClock = new util.Clock();
  text_50 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_50',
    text: 'Your decision has been submitted.\n',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  sound_1 = new sound.Sound({
      win: psychoJS.window,
      value: 'A',
      secs: 1.0,
      });
  sound_1.setVolume(1.0);
  // Initialize components for Routine "Questions"
  QuestionsClock = new util.Clock();
  text_11 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_11',
    text: 'You now will answer a few follow-up questions regarding the offer you just submitted. Your partner will NOT have access to your answers on these questions.\n\nPlease use your mouse to select your answer, and then click "continue" to move to the next question.\n\nPress SPACEBAR to begin the questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.1], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_5 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "confident"
  confidentClock = new util.Clock();
  text_12 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_12',
    text: 'If given a second chance, I would not change the offer amount I just chose.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_2 = new visual.Slider({
    win: psychoJS.window, name: 'slider_2',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["Strongly Disagree", "Disagree", "Neutral", "Agree", "Strongly Agree"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_4 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_4', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_16 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_16',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_4 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_4.mouseClock = new util.Clock();
  polygon = new visual.Rect ({
    win: psychoJS.window, name: 'polygon', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_3 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_3',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  // Initialize components for Routine "guilty"
  guiltyClock = new util.Clock();
  text_13 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_13',
    text: 'I feel guilty about the offer amount I chose.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_3 = new visual.Slider({
    win: psychoJS.window, name: 'slider_3',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["Strongly Disagree", "Disagree", "Neutral", "Agree", "Strongly Agree"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_5 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_5', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_17 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_17',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_5 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_5.mouseClock = new util.Clock();
  polygon_3 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_3', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_5 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_5',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  // Initialize components for Routine "endsmeans"
  endsmeansClock = new util.Clock();
  text_14 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_14',
    text: 'I made an offer that could seem unfair, but it is worth it to possibly get the most amount of money at the end.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_4 = new visual.Slider({
    win: psychoJS.window, name: 'slider_4',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["Strongly Disagree", "Disagree", "Neutral", "Agree", "Strongly Agree"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_6 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_6', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_18 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_18',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_6 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_6.mouseClock = new util.Clock();
  polygon_7 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_7', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_6 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_6',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  // Initialize components for Routine "rolereversal"
  rolereversalClock = new util.Clock();
  text_15 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_15',
    text: 'I would be satisfied if roles were reversed and I received my offer amount from my partner.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_5 = new visual.Slider({
    win: psychoJS.window, name: 'slider_5',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["Strongly Disagree", "Disagree", "Neutral", "Agree", "Strongly Agree"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_8 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_8', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_19 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_19',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_7 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_7.mouseClock = new util.Clock();
  polygon_11 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_11', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_20 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_20',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  // Initialize components for Routine "feel"
  feelClock = new util.Clock();
  text_21 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_21',
    text: 'I considered how my offer would make my partner feel.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_6 = new visual.Slider({
    win: psychoJS.window, name: 'slider_6',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["Strongly Disagree", "Disagree", "Neutral", "Agree", "Strongly Agree"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5],
    granularity: 0.0, style: ["RADIO"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_12 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_12', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_22 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_22',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_8 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_8.mouseClock = new util.Clock();
  polygon_13 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_13', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_23 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_23',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  // Initialize components for Routine "questions_phys"
  questions_physClock = new util.Clock();
  text_58 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_58',
    text: "The next two questions are regarding your partner's physical characteristics.\n\n If you could NOT see your partner in this round, you may skip these questions by simply clicking continue.\n\nPress SPACEBAR to begin the questions.",
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.1], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_7 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Initialize components for Routine "look2"
  look2Clock = new util.Clock();
  text_28 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_28',
    text: 'Please rate how physically attractive you found your partner from 1-7. ',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_7 = new visual.Slider({
    win: psychoJS.window, name: 'slider_7',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["1", "2", "3", "4", "5", "6", "7"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5, 6, 7],
    granularity: 0.0, style: ["RATING"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_15 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_15', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_31 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_31',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_9 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_9.mouseClock = new util.Clock();
  polygon_16 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_16', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_32 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_32',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  text_33 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_33',
    text: 'Very unattractive',
    font: 'Arial',
    units: undefined, 
    pos: [(- 0.6), (- 0.25)], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -7.0 
  });
  
  text_35 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_35',
    text: 'Very attractive',
    font: 'Arial',
    units: undefined, 
    pos: [0.6, (- 0.25)], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -8.0 
  });
  
  // Initialize components for Routine "trust"
  trustClock = new util.Clock();
  text_52 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_52',
    text: 'Please rate how trustworthy your partner looks from 1-7. ',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.15], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  slider_8 = new visual.Slider({
    win: psychoJS.window, name: 'slider_8',
    startValue: undefined,
    size: [1.25, 0.1], pos: [0, (- 0.1)], ori: 0.0, units: psychoJS.window.units,
    labels: ["1", "2", "3", "4", "5", "6", "7"], fontSize: 0.03, ticks: [1, 2, 3, 4, 5, 6, 7],
    granularity: 0.0, style: ["RATING"],
    color: new util.Color('LightGray'), markerColor: new util.Color('Red'), lineColor: new util.Color('White'), 
    opacity: undefined, fontFamily: 'Open Sans', bold: true, italic: false, depth: -1, 
    flip: false,
  });
  
  polygon_17 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_17', 
    width: [0.3, 0.1][0], height: [0.3, 0.1][1],
    ori: 0.0, pos: [0, (- 0.35)],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color('white'),
    opacity: undefined, depth: -2, interpolate: true,
  });
  
  text_53 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_53',
    text: 'Continue',
    font: 'Arial',
    units: undefined, 
    pos: [0, (- 0.35)], height: 0.04,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([(- 1.0), (- 1.0), (- 1.0)]),  opacity: undefined,
    depth: -3.0 
  });
  
  mouse_10 = new core.Mouse({
    win: psychoJS.window,
  });
  mouse_10.mouseClock = new util.Clock();
  polygon_18 = new visual.Rect ({
    win: psychoJS.window, name: 'polygon_18', 
    width: [1.0, 0.05][0], height: [1.0, 0.05][1],
    ori: 0.0, pos: [0, 0.35],
    anchor: 'center',
    lineWidth: 1.0, 
    colorSpace: 'rgb',
    lineColor: new util.Color('white'),
    fillColor: new util.Color([0.0902, (- 1.0), (- 1.0)]),
    opacity: undefined, depth: -5, interpolate: true,
  });
  
  text_54 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_54',
    text: 'Your partner will NOT have access to responses on follow up questions.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0.35], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -6.0 
  });
  
  text_55 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_55',
    text: 'Very untrustworthy',
    font: 'Arial',
    units: undefined, 
    pos: [(- 0.6), (- 0.25)], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -7.0 
  });
  
  text_56 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_56',
    text: 'Very trustworthy',
    font: 'Arial',
    units: undefined, 
    pos: [0.6, (- 0.25)], height: 0.03,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color('white'),  opacity: undefined,
    depth: -8.0 
  });
  
  // Initialize components for Routine "endofround"
  endofroundClock = new util.Clock();
  text_51 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_51',
    text: 'You have completed this round.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  sound_4 = new sound.Sound({
      win: psychoJS.window,
      value: 'A',
      secs: 1.0,
      });
  sound_4.setVolume(1.0);
  // Initialize components for Routine "End"
  EndClock = new util.Clock();
  text_4 = new visual.TextStim({
    win: psychoJS.window,
    name: 'text_4',
    text: 'You have completed the task. Thank you for participating! Press SPACEBAR to exit.',
    font: 'Arial',
    units: undefined, 
    pos: [0, 0], height: 0.05,  wrapWidth: undefined, ori: 0.0,
    languageStyle: 'LTR',
    color: new util.Color([1.0, 1.0, 1.0]),  opacity: undefined,
    depth: 0.0 
  });
  
  key_resp_2 = new core.Keyboard({psychoJS: psychoJS, clock: new util.Clock(), waitForStart: true});
  
  // Create some handy timers
  globalClock = new util.Clock();  // to track the time since experiment started
  routineTimer = new util.CountdownTimer();  // to track time remaining of each (non-slip) routine
  
  return Scheduler.Event.NEXT;
}


var t;
var frameN;
var continueRoutine;
var _key_resp_3_allKeys;
var WelcomeComponents;
function WelcomeRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'Welcome' ---
    t = 0;
    WelcomeClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('Welcome.started', globalClock.getTime());
    key_resp_3.keys = undefined;
    key_resp_3.rt = undefined;
    _key_resp_3_allKeys = [];
    // keep track of which components have finished
    WelcomeComponents = [];
    WelcomeComponents.push(text_10);
    WelcomeComponents.push(key_resp_3);
    
    for (const thisComponent of WelcomeComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function WelcomeRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'Welcome' ---
    // get current time
    t = WelcomeClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_10* updates
    if (t >= 0.0 && text_10.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_10.tStart = t;  // (not accounting for frame time here)
      text_10.frameNStart = frameN;  // exact frame index
      
      text_10.setAutoDraw(true);
    }
    
    
    // *key_resp_3* updates
    if (t >= 0.0 && key_resp_3.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_3.tStart = t;  // (not accounting for frame time here)
      key_resp_3.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_3.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_3.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_3.clearEvents(); });
    }
    
    if (key_resp_3.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_3.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_3_allKeys = _key_resp_3_allKeys.concat(theseKeys);
      if (_key_resp_3_allKeys.length > 0) {
        key_resp_3.keys = _key_resp_3_allKeys[_key_resp_3_allKeys.length - 1].name;  // just the last key pressed
        key_resp_3.rt = _key_resp_3_allKeys[_key_resp_3_allKeys.length - 1].rt;
        key_resp_3.duration = _key_resp_3_allKeys[_key_resp_3_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of WelcomeComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function WelcomeRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'Welcome' ---
    for (const thisComponent of WelcomeComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('Welcome.stopped', globalClock.getTime());
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_3.corr, level);
    }
    psychoJS.experiment.addData('key_resp_3.keys', key_resp_3.keys);
    if (typeof key_resp_3.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_3.rt', key_resp_3.rt);
        psychoJS.experiment.addData('key_resp_3.duration', key_resp_3.duration);
        routineTimer.reset();
        }
    
    key_resp_3.stop();
    // the Routine "Welcome" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var Welcome_2StartWinParams;
var _key_resp_6_allKeys;
var Welcome_2Components;
function Welcome_2RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'Welcome_2' ---
    t = 0;
    Welcome_2Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('Welcome_2.started', globalClock.getTime());
    Welcome_2StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = [(- 1.0), (- 1.0), (- 1.0)];
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_6.keys = undefined;
    key_resp_6.rt = undefined;
    _key_resp_6_allKeys = [];
    // keep track of which components have finished
    Welcome_2Components = [];
    Welcome_2Components.push(text_71);
    Welcome_2Components.push(key_resp_6);
    
    for (const thisComponent of Welcome_2Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function Welcome_2RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'Welcome_2' ---
    // get current time
    t = Welcome_2Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_71* updates
    if (t >= 0.0 && text_71.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_71.tStart = t;  // (not accounting for frame time here)
      text_71.frameNStart = frameN;  // exact frame index
      
      text_71.setAutoDraw(true);
    }
    
    
    // *key_resp_6* updates
    if (t >= 0.0 && key_resp_6.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_6.tStart = t;  // (not accounting for frame time here)
      key_resp_6.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_6.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_6.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_6.clearEvents(); });
    }
    
    if (key_resp_6.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_6.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_6_allKeys = _key_resp_6_allKeys.concat(theseKeys);
      if (_key_resp_6_allKeys.length > 0) {
        key_resp_6.keys = _key_resp_6_allKeys[_key_resp_6_allKeys.length - 1].name;  // just the last key pressed
        key_resp_6.rt = _key_resp_6_allKeys[_key_resp_6_allKeys.length - 1].rt;
        key_resp_6.duration = _key_resp_6_allKeys[_key_resp_6_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of Welcome_2Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function Welcome_2RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'Welcome_2' ---
    for (const thisComponent of Welcome_2Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('Welcome_2.stopped', globalClock.getTime());
    psychoJS.window.color = Welcome_2StartWinParams['color'];
    psychoJS.window.colorSpace = Welcome_2StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = Welcome_2StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = Welcome_2StartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_6.corr, level);
    }
    psychoJS.experiment.addData('key_resp_6.keys', key_resp_6.keys);
    if (typeof key_resp_6.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_6.rt', key_resp_6.rt);
        psychoJS.experiment.addData('key_resp_6.duration', key_resp_6.duration);
        routineTimer.reset();
        }
    
    key_resp_6.stop();
    // the Routine "Welcome_2" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var instructions1StartWinParams;
var _key_resp_13_allKeys;
var instructions1Components;
function instructions1RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'instructions1' ---
    t = 0;
    instructions1Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('instructions1.started', globalClock.getTime());
    instructions1StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_13.keys = undefined;
    key_resp_13.rt = undefined;
    _key_resp_13_allKeys = [];
    // keep track of which components have finished
    instructions1Components = [];
    instructions1Components.push(text_29);
    instructions1Components.push(key_resp_13);
    
    for (const thisComponent of instructions1Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function instructions1RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'instructions1' ---
    // get current time
    t = instructions1Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_29* updates
    if (t >= 0.0 && text_29.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_29.tStart = t;  // (not accounting for frame time here)
      text_29.frameNStart = frameN;  // exact frame index
      
      text_29.setAutoDraw(true);
    }
    
    
    // *key_resp_13* updates
    if (t >= 0.0 && key_resp_13.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_13.tStart = t;  // (not accounting for frame time here)
      key_resp_13.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_13.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_13.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_13.clearEvents(); });
    }
    
    if (key_resp_13.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_13.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_13_allKeys = _key_resp_13_allKeys.concat(theseKeys);
      if (_key_resp_13_allKeys.length > 0) {
        key_resp_13.keys = _key_resp_13_allKeys[_key_resp_13_allKeys.length - 1].name;  // just the last key pressed
        key_resp_13.rt = _key_resp_13_allKeys[_key_resp_13_allKeys.length - 1].rt;
        key_resp_13.duration = _key_resp_13_allKeys[_key_resp_13_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of instructions1Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function instructions1RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'instructions1' ---
    for (const thisComponent of instructions1Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('instructions1.stopped', globalClock.getTime());
    psychoJS.window.color = instructions1StartWinParams['color'];
    psychoJS.window.colorSpace = instructions1StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = instructions1StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = instructions1StartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_13.corr, level);
    }
    psychoJS.experiment.addData('key_resp_13.keys', key_resp_13.keys);
    if (typeof key_resp_13.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_13.rt', key_resp_13.rt);
        psychoJS.experiment.addData('key_resp_13.duration', key_resp_13.duration);
        routineTimer.reset();
        }
    
    key_resp_13.stop();
    // the Routine "instructions1" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var practice_decisionStartWinParams;
var gotValidClick;
var practice_decisionComponents;
function practice_decisionRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'practice_decision' ---
    t = 0;
    practice_decisionClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('practice_decision.started', globalClock.getTime());
    practice_decisionStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_12.reset()
    // setup some python lists for storing info about the mouse_2
    // current position of the mouse:
    mouse_2.x = [];
    mouse_2.y = [];
    mouse_2.leftButton = [];
    mouse_2.midButton = [];
    mouse_2.rightButton = [];
    mouse_2.time = [];
    mouse_2.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    practice_decisionComponents = [];
    practice_decisionComponents.push(text_30);
    practice_decisionComponents.push(slider_12);
    practice_decisionComponents.push(polygon_2);
    practice_decisionComponents.push(text_8);
    practice_decisionComponents.push(mouse_2);
    
    for (const thisComponent of practice_decisionComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


var prevButtonState;
var _mouseButtons;
var _mouseXYs;
function practice_decisionRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'practice_decision' ---
    // get current time
    t = practice_decisionClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_30* updates
    if (t >= 0.0 && text_30.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_30.tStart = t;  // (not accounting for frame time here)
      text_30.frameNStart = frameN;  // exact frame index
      
      text_30.setAutoDraw(true);
    }
    
    
    // *slider_12* updates
    if (t >= 0.0 && slider_12.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_12.tStart = t;  // (not accounting for frame time here)
      slider_12.frameNStart = frameN;  // exact frame index
      
      slider_12.setAutoDraw(true);
    }
    
    
    // *polygon_2* updates
    if (t >= 0.0 && polygon_2.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_2.tStart = t;  // (not accounting for frame time here)
      polygon_2.frameNStart = frameN;  // exact frame index
      
      polygon_2.setAutoDraw(true);
    }
    
    
    // *text_8* updates
    if (t >= 0.0 && text_8.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_8.tStart = t;  // (not accounting for frame time here)
      text_8.frameNStart = frameN;  // exact frame index
      
      text_8.setAutoDraw(true);
    }
    
    // *mouse_2* updates
    if (t >= 0.0 && mouse_2.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_2.tStart = t;  // (not accounting for frame time here)
      mouse_2.frameNStart = frameN;  // exact frame index
      
      mouse_2.status = PsychoJS.Status.STARTED;
      mouse_2.mouseClock.reset();
      prevButtonState = mouse_2.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_2.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_2.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_2]) {
            if (obj.contains(mouse_2)) {
              gotValidClick = true;
              mouse_2.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_2.getPos();
          mouse_2.x.push(_mouseXYs[0]);
          mouse_2.y.push(_mouseXYs[1]);
          mouse_2.leftButton.push(_mouseButtons[0]);
          mouse_2.midButton.push(_mouseButtons[1]);
          mouse_2.rightButton.push(_mouseButtons[2]);
          mouse_2.time.push(mouse_2.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of practice_decisionComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function practice_decisionRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'practice_decision' ---
    for (const thisComponent of practice_decisionComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('practice_decision.stopped', globalClock.getTime());
    psychoJS.window.color = practice_decisionStartWinParams['color'];
    psychoJS.window.colorSpace = practice_decisionStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = practice_decisionStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = practice_decisionStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_12.response', slider_12.getRating());
    psychoJS.experiment.addData('slider_12.rt', slider_12.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_2.x) {  psychoJS.experiment.addData('mouse_2.x', mouse_2.x[0])};
    if (mouse_2.y) {  psychoJS.experiment.addData('mouse_2.y', mouse_2.y[0])};
    if (mouse_2.leftButton) {  psychoJS.experiment.addData('mouse_2.leftButton', mouse_2.leftButton[0])};
    if (mouse_2.midButton) {  psychoJS.experiment.addData('mouse_2.midButton', mouse_2.midButton[0])};
    if (mouse_2.rightButton) {  psychoJS.experiment.addData('mouse_2.rightButton', mouse_2.rightButton[0])};
    if (mouse_2.time) {  psychoJS.experiment.addData('mouse_2.time', mouse_2.time[0])};
    if (mouse_2.clicked_name) {  psychoJS.experiment.addData('mouse_2.clicked_name', mouse_2.clicked_name[0])};
    
    // the Routine "practice_decision" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var instructions2StartWinParams;
var _key_resp_16_allKeys;
var instructions2Components;
function instructions2RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'instructions2' ---
    t = 0;
    instructions2Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('instructions2.started', globalClock.getTime());
    instructions2StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_16.keys = undefined;
    key_resp_16.rt = undefined;
    _key_resp_16_allKeys = [];
    // keep track of which components have finished
    instructions2Components = [];
    instructions2Components.push(text_34);
    instructions2Components.push(key_resp_16);
    
    for (const thisComponent of instructions2Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function instructions2RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'instructions2' ---
    // get current time
    t = instructions2Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_34* updates
    if (t >= 0.0 && text_34.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_34.tStart = t;  // (not accounting for frame time here)
      text_34.frameNStart = frameN;  // exact frame index
      
      text_34.setAutoDraw(true);
    }
    
    
    // *key_resp_16* updates
    if (t >= 0.0 && key_resp_16.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_16.tStart = t;  // (not accounting for frame time here)
      key_resp_16.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_16.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_16.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_16.clearEvents(); });
    }
    
    if (key_resp_16.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_16.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_16_allKeys = _key_resp_16_allKeys.concat(theseKeys);
      if (_key_resp_16_allKeys.length > 0) {
        key_resp_16.keys = _key_resp_16_allKeys[_key_resp_16_allKeys.length - 1].name;  // just the last key pressed
        key_resp_16.rt = _key_resp_16_allKeys[_key_resp_16_allKeys.length - 1].rt;
        key_resp_16.duration = _key_resp_16_allKeys[_key_resp_16_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of instructions2Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function instructions2RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'instructions2' ---
    for (const thisComponent of instructions2Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('instructions2.stopped', globalClock.getTime());
    psychoJS.window.color = instructions2StartWinParams['color'];
    psychoJS.window.colorSpace = instructions2StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = instructions2StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = instructions2StartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_16.corr, level);
    }
    psychoJS.experiment.addData('key_resp_16.keys', key_resp_16.keys);
    if (typeof key_resp_16.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_16.rt', key_resp_16.rt);
        psychoJS.experiment.addData('key_resp_16.duration', key_resp_16.duration);
        routineTimer.reset();
        }
    
    key_resp_16.stop();
    // the Routine "instructions2" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var sound_2StartWinParams;
var sound_2Components;
function sound_2RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'sound_2' ---
    t = 0;
    sound_2Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    routineTimer.add(3.000000);
    // update component parameters for each repeat
    psychoJS.experiment.addData('sound_2.started', globalClock.getTime());
    sound_2StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    sound_3.secs=1.0;
    sound_3.setVolume(1.0);
    // keep track of which components have finished
    sound_2Components = [];
    sound_2Components.push(text);
    sound_2Components.push(sound_3);
    
    for (const thisComponent of sound_2Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


var frameRemains;
function sound_2RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'sound_2' ---
    // get current time
    t = sound_2Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text* updates
    if (t >= 0.0 && text.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text.tStart = t;  // (not accounting for frame time here)
      text.frameNStart = frameN;  // exact frame index
      
      text.setAutoDraw(true);
    }
    
    frameRemains = 0.0 + 3 - psychoJS.window.monitorFramePeriod * 0.75;  // most of one frame period left
    if (text.status === PsychoJS.Status.STARTED && t >= frameRemains) {
      text.setAutoDraw(false);
    }
    // start/stop sound_3
    if (t >= 0.0 && sound_3.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      sound_3.tStart = t;  // (not accounting for frame time here)
      sound_3.frameNStart = frameN;  // exact frame index
      
      psychoJS.window.callOnFlip(function(){ sound_3.play(); });  // screen flip
      sound_3.status = PsychoJS.Status.STARTED;
    }
    frameRemains = 0.0 + 1.0 - psychoJS.window.monitorFramePeriod * 0.75;  // most of one frame period left
    if (sound_3.status === PsychoJS.Status.STARTED && t >= frameRemains) {
      if (t >= sound_3.tStart + 0.5) {
        sound_3.stop();  // stop the sound (if longer than duration)
        sound_3.status = PsychoJS.Status.FINISHED;
      }
    }
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of sound_2Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine && routineTimer.getTime() > 0) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function sound_2RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'sound_2' ---
    for (const thisComponent of sound_2Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('sound_2.stopped', globalClock.getTime());
    psychoJS.window.color = sound_2StartWinParams['color'];
    psychoJS.window.colorSpace = sound_2StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = sound_2StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = sound_2StartWinParams['backgroundFit'];
    sound_3.stop();  // ensure sound has stopped at end of Routine
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var instructions2_3StartWinParams;
var _key_resp_31_allKeys;
var instructions2_3Components;
function instructions2_3RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'instructions2_3' ---
    t = 0;
    instructions2_3Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('instructions2_3.started', globalClock.getTime());
    instructions2_3StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_31.keys = undefined;
    key_resp_31.rt = undefined;
    _key_resp_31_allKeys = [];
    // keep track of which components have finished
    instructions2_3Components = [];
    instructions2_3Components.push(text_49);
    instructions2_3Components.push(key_resp_31);
    
    for (const thisComponent of instructions2_3Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function instructions2_3RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'instructions2_3' ---
    // get current time
    t = instructions2_3Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_49* updates
    if (t >= 0.0 && text_49.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_49.tStart = t;  // (not accounting for frame time here)
      text_49.frameNStart = frameN;  // exact frame index
      
      text_49.setAutoDraw(true);
    }
    
    
    // *key_resp_31* updates
    if (t >= 0.0 && key_resp_31.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_31.tStart = t;  // (not accounting for frame time here)
      key_resp_31.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_31.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_31.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_31.clearEvents(); });
    }
    
    if (key_resp_31.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_31.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_31_allKeys = _key_resp_31_allKeys.concat(theseKeys);
      if (_key_resp_31_allKeys.length > 0) {
        key_resp_31.keys = _key_resp_31_allKeys[_key_resp_31_allKeys.length - 1].name;  // just the last key pressed
        key_resp_31.rt = _key_resp_31_allKeys[_key_resp_31_allKeys.length - 1].rt;
        key_resp_31.duration = _key_resp_31_allKeys[_key_resp_31_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of instructions2_3Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function instructions2_3RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'instructions2_3' ---
    for (const thisComponent of instructions2_3Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('instructions2_3.stopped', globalClock.getTime());
    psychoJS.window.color = instructions2_3StartWinParams['color'];
    psychoJS.window.colorSpace = instructions2_3StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = instructions2_3StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = instructions2_3StartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_31.corr, level);
    }
    psychoJS.experiment.addData('key_resp_31.keys', key_resp_31.keys);
    if (typeof key_resp_31.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_31.rt', key_resp_31.rt);
        psychoJS.experiment.addData('key_resp_31.duration', key_resp_31.duration);
        routineTimer.reset();
        }
    
    key_resp_31.stop();
    // the Routine "instructions2_3" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var trials;
function trialsLoopBegin(trialsLoopScheduler, snapshot) {
  return async function() {
    TrialHandler.fromSnapshot(snapshot); // update internal variables (.thisN etc) of the loop
    
    // set up handler to look after randomisation of conditions etc
    trials = new TrialHandler({
      psychoJS: psychoJS,
      nReps: 4, method: TrialHandler.Method.SEQUENTIAL,
      extraInfo: expInfo, originPath: undefined,
      trialList: undefined,
      seed: undefined, name: 'trials'
    });
    psychoJS.experiment.addLoop(trials); // add the loop to the experiment
    currentLoop = trials;  // we're now the current loop
    
    // Schedule all the trials in the trialList:
    for (const thisTrial of trials) {
      snapshot = trials.getSnapshot();
      trialsLoopScheduler.add(importConditions(snapshot));
      trialsLoopScheduler.add(begin_roundRoutineBegin(snapshot));
      trialsLoopScheduler.add(begin_roundRoutineEachFrame());
      trialsLoopScheduler.add(begin_roundRoutineEnd(snapshot));
      trialsLoopScheduler.add(Wait_2RoutineBegin(snapshot));
      trialsLoopScheduler.add(Wait_2RoutineEachFrame());
      trialsLoopScheduler.add(Wait_2RoutineEnd(snapshot));
      trialsLoopScheduler.add(DecisionRoutineBegin(snapshot));
      trialsLoopScheduler.add(DecisionRoutineEachFrame());
      trialsLoopScheduler.add(DecisionRoutineEnd(snapshot));
      trialsLoopScheduler.add(decisionmadeRoutineBegin(snapshot));
      trialsLoopScheduler.add(decisionmadeRoutineEachFrame());
      trialsLoopScheduler.add(decisionmadeRoutineEnd(snapshot));
      trialsLoopScheduler.add(QuestionsRoutineBegin(snapshot));
      trialsLoopScheduler.add(QuestionsRoutineEachFrame());
      trialsLoopScheduler.add(QuestionsRoutineEnd(snapshot));
      trialsLoopScheduler.add(confidentRoutineBegin(snapshot));
      trialsLoopScheduler.add(confidentRoutineEachFrame());
      trialsLoopScheduler.add(confidentRoutineEnd(snapshot));
      trialsLoopScheduler.add(guiltyRoutineBegin(snapshot));
      trialsLoopScheduler.add(guiltyRoutineEachFrame());
      trialsLoopScheduler.add(guiltyRoutineEnd(snapshot));
      trialsLoopScheduler.add(endsmeansRoutineBegin(snapshot));
      trialsLoopScheduler.add(endsmeansRoutineEachFrame());
      trialsLoopScheduler.add(endsmeansRoutineEnd(snapshot));
      trialsLoopScheduler.add(rolereversalRoutineBegin(snapshot));
      trialsLoopScheduler.add(rolereversalRoutineEachFrame());
      trialsLoopScheduler.add(rolereversalRoutineEnd(snapshot));
      trialsLoopScheduler.add(feelRoutineBegin(snapshot));
      trialsLoopScheduler.add(feelRoutineEachFrame());
      trialsLoopScheduler.add(feelRoutineEnd(snapshot));
      trialsLoopScheduler.add(questions_physRoutineBegin(snapshot));
      trialsLoopScheduler.add(questions_physRoutineEachFrame());
      trialsLoopScheduler.add(questions_physRoutineEnd(snapshot));
      trialsLoopScheduler.add(look2RoutineBegin(snapshot));
      trialsLoopScheduler.add(look2RoutineEachFrame());
      trialsLoopScheduler.add(look2RoutineEnd(snapshot));
      trialsLoopScheduler.add(trustRoutineBegin(snapshot));
      trialsLoopScheduler.add(trustRoutineEachFrame());
      trialsLoopScheduler.add(trustRoutineEnd(snapshot));
      trialsLoopScheduler.add(endofroundRoutineBegin(snapshot));
      trialsLoopScheduler.add(endofroundRoutineEachFrame());
      trialsLoopScheduler.add(endofroundRoutineEnd(snapshot));
      trialsLoopScheduler.add(trialsLoopEndIteration(trialsLoopScheduler, snapshot));
    }
    
    return Scheduler.Event.NEXT;
  }
}


async function trialsLoopEnd() {
  // terminate loop
  psychoJS.experiment.removeLoop(trials);
  // update the current loop from the ExperimentHandler
  if (psychoJS.experiment._unfinishedLoops.length>0)
    currentLoop = psychoJS.experiment._unfinishedLoops.at(-1);
  else
    currentLoop = psychoJS.experiment;  // so we use addData from the experiment
  return Scheduler.Event.NEXT;
}


function trialsLoopEndIteration(scheduler, snapshot) {
  // ------Prepare for next entry------
  return async function () {
    if (typeof snapshot !== 'undefined') {
      // ------Check if user ended loop early------
      if (snapshot.finished) {
        // Check for and save orphaned data
        if (psychoJS.experiment.isEntryEmpty()) {
          psychoJS.experiment.nextEntry(snapshot);
        }
        scheduler.stop();
      } else {
        psychoJS.experiment.nextEntry(snapshot);
      }
    return Scheduler.Event.NEXT;
    }
  };
}


var begin_roundStartWinParams;
var _key_resp_40_allKeys;
var begin_roundComponents;
function begin_roundRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'begin_round' ---
    t = 0;
    begin_roundClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('begin_round.started', globalClock.getTime());
    begin_roundStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = [0.0039, (- 1.0), (- 1.0)];
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_40.keys = undefined;
    key_resp_40.rt = undefined;
    _key_resp_40_allKeys = [];
    // keep track of which components have finished
    begin_roundComponents = [];
    begin_roundComponents.push(polygon_9);
    begin_roundComponents.push(text_47);
    begin_roundComponents.push(text_70);
    begin_roundComponents.push(key_resp_40);
    
    for (const thisComponent of begin_roundComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function begin_roundRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'begin_round' ---
    // get current time
    t = begin_roundClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *polygon_9* updates
    if (t >= 0.0 && polygon_9.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_9.tStart = t;  // (not accounting for frame time here)
      polygon_9.frameNStart = frameN;  // exact frame index
      
      polygon_9.setAutoDraw(true);
    }
    
    
    // *text_47* updates
    if (t >= 0.0 && text_47.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_47.tStart = t;  // (not accounting for frame time here)
      text_47.frameNStart = frameN;  // exact frame index
      
      text_47.setAutoDraw(true);
    }
    
    
    // *text_70* updates
    if (t >= 0.0 && text_70.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_70.tStart = t;  // (not accounting for frame time here)
      text_70.frameNStart = frameN;  // exact frame index
      
      text_70.setAutoDraw(true);
    }
    
    
    // *key_resp_40* updates
    if (t >= 0.0 && key_resp_40.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_40.tStart = t;  // (not accounting for frame time here)
      key_resp_40.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_40.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_40.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_40.clearEvents(); });
    }
    
    if (key_resp_40.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_40.getKeys({keyList: ['q', 'z'], waitRelease: false});
      _key_resp_40_allKeys = _key_resp_40_allKeys.concat(theseKeys);
      if (_key_resp_40_allKeys.length > 0) {
        key_resp_40.keys = _key_resp_40_allKeys[_key_resp_40_allKeys.length - 1].name;  // just the last key pressed
        key_resp_40.rt = _key_resp_40_allKeys[_key_resp_40_allKeys.length - 1].rt;
        key_resp_40.duration = _key_resp_40_allKeys[_key_resp_40_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of begin_roundComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function begin_roundRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'begin_round' ---
    for (const thisComponent of begin_roundComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('begin_round.stopped', globalClock.getTime());
    psychoJS.window.color = begin_roundStartWinParams['color'];
    psychoJS.window.colorSpace = begin_roundStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = begin_roundStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = begin_roundStartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_40.corr, level);
    }
    psychoJS.experiment.addData('key_resp_40.keys', key_resp_40.keys);
    if (typeof key_resp_40.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_40.rt', key_resp_40.rt);
        psychoJS.experiment.addData('key_resp_40.duration', key_resp_40.duration);
        routineTimer.reset();
        }
    
    key_resp_40.stop();
    // the Routine "begin_round" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var Wait_2StartWinParams;
var _key_resp_29_allKeys;
var Wait_2Components;
function Wait_2RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'Wait_2' ---
    t = 0;
    Wait_2Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('Wait_2.started', globalClock.getTime());
    Wait_2StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_29.keys = undefined;
    key_resp_29.rt = undefined;
    _key_resp_29_allKeys = [];
    // keep track of which components have finished
    Wait_2Components = [];
    Wait_2Components.push(text_9);
    Wait_2Components.push(key_resp_29);
    
    for (const thisComponent of Wait_2Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function Wait_2RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'Wait_2' ---
    // get current time
    t = Wait_2Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_9* updates
    if (t >= 0.0 && text_9.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_9.tStart = t;  // (not accounting for frame time here)
      text_9.frameNStart = frameN;  // exact frame index
      
      text_9.setAutoDraw(true);
    }
    
    
    // *key_resp_29* updates
    if (t >= 0.0 && key_resp_29.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_29.tStart = t;  // (not accounting for frame time here)
      key_resp_29.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_29.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_29.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_29.clearEvents(); });
    }
    
    if (key_resp_29.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_29.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_29_allKeys = _key_resp_29_allKeys.concat(theseKeys);
      if (_key_resp_29_allKeys.length > 0) {
        key_resp_29.keys = _key_resp_29_allKeys[_key_resp_29_allKeys.length - 1].name;  // just the last key pressed
        key_resp_29.rt = _key_resp_29_allKeys[_key_resp_29_allKeys.length - 1].rt;
        key_resp_29.duration = _key_resp_29_allKeys[_key_resp_29_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of Wait_2Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function Wait_2RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'Wait_2' ---
    for (const thisComponent of Wait_2Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('Wait_2.stopped', globalClock.getTime());
    psychoJS.window.color = Wait_2StartWinParams['color'];
    psychoJS.window.colorSpace = Wait_2StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = Wait_2StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = Wait_2StartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_29.corr, level);
    }
    psychoJS.experiment.addData('key_resp_29.keys', key_resp_29.keys);
    if (typeof key_resp_29.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_29.rt', key_resp_29.rt);
        psychoJS.experiment.addData('key_resp_29.duration', key_resp_29.duration);
        routineTimer.reset();
        }
    
    key_resp_29.stop();
    // the Routine "Wait_2" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var DecisionStartWinParams;
var DecisionComponents;
function DecisionRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'Decision' ---
    t = 0;
    DecisionClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('Decision.started', globalClock.getTime());
    DecisionStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider.reset()
    // setup some python lists for storing info about the mouse
    // current position of the mouse:
    mouse.x = [];
    mouse.y = [];
    mouse.leftButton = [];
    mouse.midButton = [];
    mouse.rightButton = [];
    mouse.time = [];
    mouse.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    DecisionComponents = [];
    DecisionComponents.push(text_2);
    DecisionComponents.push(slider);
    DecisionComponents.push(polygon_10);
    DecisionComponents.push(text_7);
    DecisionComponents.push(mouse);
    
    for (const thisComponent of DecisionComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function DecisionRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'Decision' ---
    // get current time
    t = DecisionClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_2* updates
    if (t >= 0.0 && text_2.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_2.tStart = t;  // (not accounting for frame time here)
      text_2.frameNStart = frameN;  // exact frame index
      
      text_2.setAutoDraw(true);
    }
    
    
    // *slider* updates
    if (t >= 0.0 && slider.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider.tStart = t;  // (not accounting for frame time here)
      slider.frameNStart = frameN;  // exact frame index
      
      slider.setAutoDraw(true);
    }
    
    
    // *polygon_10* updates
    if (t >= 0.0 && polygon_10.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_10.tStart = t;  // (not accounting for frame time here)
      polygon_10.frameNStart = frameN;  // exact frame index
      
      polygon_10.setAutoDraw(true);
    }
    
    
    // *text_7* updates
    if (t >= 0.0 && text_7.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_7.tStart = t;  // (not accounting for frame time here)
      text_7.frameNStart = frameN;  // exact frame index
      
      text_7.setAutoDraw(true);
    }
    
    // *mouse* updates
    if (t >= 0.0 && mouse.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse.tStart = t;  // (not accounting for frame time here)
      mouse.frameNStart = frameN;  // exact frame index
      
      mouse.status = PsychoJS.Status.STARTED;
      mouse.mouseClock.reset();
      prevButtonState = mouse.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_10]) {
            if (obj.contains(mouse)) {
              gotValidClick = true;
              mouse.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse.getPos();
          mouse.x.push(_mouseXYs[0]);
          mouse.y.push(_mouseXYs[1]);
          mouse.leftButton.push(_mouseButtons[0]);
          mouse.midButton.push(_mouseButtons[1]);
          mouse.rightButton.push(_mouseButtons[2]);
          mouse.time.push(mouse.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of DecisionComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function DecisionRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'Decision' ---
    for (const thisComponent of DecisionComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('Decision.stopped', globalClock.getTime());
    psychoJS.window.color = DecisionStartWinParams['color'];
    psychoJS.window.colorSpace = DecisionStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = DecisionStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = DecisionStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider.response', slider.getRating());
    psychoJS.experiment.addData('slider.rt', slider.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse.x) {  psychoJS.experiment.addData('mouse.x', mouse.x[0])};
    if (mouse.y) {  psychoJS.experiment.addData('mouse.y', mouse.y[0])};
    if (mouse.leftButton) {  psychoJS.experiment.addData('mouse.leftButton', mouse.leftButton[0])};
    if (mouse.midButton) {  psychoJS.experiment.addData('mouse.midButton', mouse.midButton[0])};
    if (mouse.rightButton) {  psychoJS.experiment.addData('mouse.rightButton', mouse.rightButton[0])};
    if (mouse.time) {  psychoJS.experiment.addData('mouse.time', mouse.time[0])};
    if (mouse.clicked_name) {  psychoJS.experiment.addData('mouse.clicked_name', mouse.clicked_name[0])};
    
    // the Routine "Decision" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var decisionmadeStartWinParams;
var decisionmadeComponents;
function decisionmadeRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'decisionmade' ---
    t = 0;
    decisionmadeClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    routineTimer.add(5.000000);
    // update component parameters for each repeat
    psychoJS.experiment.addData('decisionmade.started', globalClock.getTime());
    decisionmadeStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    sound_1.secs=1.0;
    sound_1.setVolume(1.0);
    // keep track of which components have finished
    decisionmadeComponents = [];
    decisionmadeComponents.push(text_50);
    decisionmadeComponents.push(sound_1);
    
    for (const thisComponent of decisionmadeComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function decisionmadeRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'decisionmade' ---
    // get current time
    t = decisionmadeClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_50* updates
    if (t >= 0.0 && text_50.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_50.tStart = t;  // (not accounting for frame time here)
      text_50.frameNStart = frameN;  // exact frame index
      
      text_50.setAutoDraw(true);
    }
    
    frameRemains = 0.0 + 5 - psychoJS.window.monitorFramePeriod * 0.75;  // most of one frame period left
    if (text_50.status === PsychoJS.Status.STARTED && t >= frameRemains) {
      text_50.setAutoDraw(false);
    }
    // start/stop sound_1
    if (t >= 0.0 && sound_1.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      sound_1.tStart = t;  // (not accounting for frame time here)
      sound_1.frameNStart = frameN;  // exact frame index
      
      psychoJS.window.callOnFlip(function(){ sound_1.play(); });  // screen flip
      sound_1.status = PsychoJS.Status.STARTED;
    }
    frameRemains = 0.0 + 1.0 - psychoJS.window.monitorFramePeriod * 0.75;  // most of one frame period left
    if (sound_1.status === PsychoJS.Status.STARTED && t >= frameRemains) {
      if (t >= sound_1.tStart + 0.5) {
        sound_1.stop();  // stop the sound (if longer than duration)
        sound_1.status = PsychoJS.Status.FINISHED;
      }
    }
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of decisionmadeComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine && routineTimer.getTime() > 0) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function decisionmadeRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'decisionmade' ---
    for (const thisComponent of decisionmadeComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('decisionmade.stopped', globalClock.getTime());
    psychoJS.window.color = decisionmadeStartWinParams['color'];
    psychoJS.window.colorSpace = decisionmadeStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = decisionmadeStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = decisionmadeStartWinParams['backgroundFit'];
    sound_1.stop();  // ensure sound has stopped at end of Routine
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var QuestionsStartWinParams;
var _key_resp_5_allKeys;
var QuestionsComponents;
function QuestionsRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'Questions' ---
    t = 0;
    QuestionsClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('Questions.started', globalClock.getTime());
    QuestionsStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_5.keys = undefined;
    key_resp_5.rt = undefined;
    _key_resp_5_allKeys = [];
    // keep track of which components have finished
    QuestionsComponents = [];
    QuestionsComponents.push(text_11);
    QuestionsComponents.push(key_resp_5);
    
    for (const thisComponent of QuestionsComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function QuestionsRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'Questions' ---
    // get current time
    t = QuestionsClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_11* updates
    if (t >= 0.0 && text_11.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_11.tStart = t;  // (not accounting for frame time here)
      text_11.frameNStart = frameN;  // exact frame index
      
      text_11.setAutoDraw(true);
    }
    
    
    // *key_resp_5* updates
    if (t >= 0.0 && key_resp_5.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_5.tStart = t;  // (not accounting for frame time here)
      key_resp_5.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_5.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_5.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_5.clearEvents(); });
    }
    
    if (key_resp_5.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_5.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_5_allKeys = _key_resp_5_allKeys.concat(theseKeys);
      if (_key_resp_5_allKeys.length > 0) {
        key_resp_5.keys = _key_resp_5_allKeys[_key_resp_5_allKeys.length - 1].name;  // just the last key pressed
        key_resp_5.rt = _key_resp_5_allKeys[_key_resp_5_allKeys.length - 1].rt;
        key_resp_5.duration = _key_resp_5_allKeys[_key_resp_5_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of QuestionsComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function QuestionsRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'Questions' ---
    for (const thisComponent of QuestionsComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('Questions.stopped', globalClock.getTime());
    psychoJS.window.color = QuestionsStartWinParams['color'];
    psychoJS.window.colorSpace = QuestionsStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = QuestionsStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = QuestionsStartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_5.corr, level);
    }
    psychoJS.experiment.addData('key_resp_5.keys', key_resp_5.keys);
    if (typeof key_resp_5.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_5.rt', key_resp_5.rt);
        psychoJS.experiment.addData('key_resp_5.duration', key_resp_5.duration);
        routineTimer.reset();
        }
    
    key_resp_5.stop();
    // the Routine "Questions" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var confidentStartWinParams;
var confidentComponents;
function confidentRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'confident' ---
    t = 0;
    confidentClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('confident.started', globalClock.getTime());
    confidentStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_2.reset()
    // setup some python lists for storing info about the mouse_4
    // current position of the mouse:
    mouse_4.x = [];
    mouse_4.y = [];
    mouse_4.leftButton = [];
    mouse_4.midButton = [];
    mouse_4.rightButton = [];
    mouse_4.time = [];
    mouse_4.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    confidentComponents = [];
    confidentComponents.push(text_12);
    confidentComponents.push(slider_2);
    confidentComponents.push(polygon_4);
    confidentComponents.push(text_16);
    confidentComponents.push(mouse_4);
    confidentComponents.push(polygon);
    confidentComponents.push(text_3);
    
    for (const thisComponent of confidentComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function confidentRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'confident' ---
    // get current time
    t = confidentClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_12* updates
    if (t >= 0.0 && text_12.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_12.tStart = t;  // (not accounting for frame time here)
      text_12.frameNStart = frameN;  // exact frame index
      
      text_12.setAutoDraw(true);
    }
    
    
    // *slider_2* updates
    if (t >= 0.0 && slider_2.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_2.tStart = t;  // (not accounting for frame time here)
      slider_2.frameNStart = frameN;  // exact frame index
      
      slider_2.setAutoDraw(true);
    }
    
    
    // *polygon_4* updates
    if (t >= 0.0 && polygon_4.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_4.tStart = t;  // (not accounting for frame time here)
      polygon_4.frameNStart = frameN;  // exact frame index
      
      polygon_4.setAutoDraw(true);
    }
    
    
    // *text_16* updates
    if (t >= 0.0 && text_16.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_16.tStart = t;  // (not accounting for frame time here)
      text_16.frameNStart = frameN;  // exact frame index
      
      text_16.setAutoDraw(true);
    }
    
    // *mouse_4* updates
    if (t >= 0.0 && mouse_4.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_4.tStart = t;  // (not accounting for frame time here)
      mouse_4.frameNStart = frameN;  // exact frame index
      
      mouse_4.status = PsychoJS.Status.STARTED;
      mouse_4.mouseClock.reset();
      prevButtonState = mouse_4.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_4.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_4.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_4)) {
              gotValidClick = true;
              mouse_4.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_4.getPos();
          mouse_4.x.push(_mouseXYs[0]);
          mouse_4.y.push(_mouseXYs[1]);
          mouse_4.leftButton.push(_mouseButtons[0]);
          mouse_4.midButton.push(_mouseButtons[1]);
          mouse_4.rightButton.push(_mouseButtons[2]);
          mouse_4.time.push(mouse_4.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon* updates
    if (t >= 0.0 && polygon.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon.tStart = t;  // (not accounting for frame time here)
      polygon.frameNStart = frameN;  // exact frame index
      
      polygon.setAutoDraw(true);
    }
    
    
    // *text_3* updates
    if (t >= 0.0 && text_3.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_3.tStart = t;  // (not accounting for frame time here)
      text_3.frameNStart = frameN;  // exact frame index
      
      text_3.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of confidentComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function confidentRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'confident' ---
    for (const thisComponent of confidentComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('confident.stopped', globalClock.getTime());
    psychoJS.window.color = confidentStartWinParams['color'];
    psychoJS.window.colorSpace = confidentStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = confidentStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = confidentStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_2.response', slider_2.getRating());
    psychoJS.experiment.addData('slider_2.rt', slider_2.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_4.x) {  psychoJS.experiment.addData('mouse_4.x', mouse_4.x[0])};
    if (mouse_4.y) {  psychoJS.experiment.addData('mouse_4.y', mouse_4.y[0])};
    if (mouse_4.leftButton) {  psychoJS.experiment.addData('mouse_4.leftButton', mouse_4.leftButton[0])};
    if (mouse_4.midButton) {  psychoJS.experiment.addData('mouse_4.midButton', mouse_4.midButton[0])};
    if (mouse_4.rightButton) {  psychoJS.experiment.addData('mouse_4.rightButton', mouse_4.rightButton[0])};
    if (mouse_4.time) {  psychoJS.experiment.addData('mouse_4.time', mouse_4.time[0])};
    if (mouse_4.clicked_name) {  psychoJS.experiment.addData('mouse_4.clicked_name', mouse_4.clicked_name[0])};
    
    // the Routine "confident" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var guiltyStartWinParams;
var guiltyComponents;
function guiltyRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'guilty' ---
    t = 0;
    guiltyClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('guilty.started', globalClock.getTime());
    guiltyStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_3.reset()
    // setup some python lists for storing info about the mouse_5
    // current position of the mouse:
    mouse_5.x = [];
    mouse_5.y = [];
    mouse_5.leftButton = [];
    mouse_5.midButton = [];
    mouse_5.rightButton = [];
    mouse_5.time = [];
    mouse_5.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    guiltyComponents = [];
    guiltyComponents.push(text_13);
    guiltyComponents.push(slider_3);
    guiltyComponents.push(polygon_5);
    guiltyComponents.push(text_17);
    guiltyComponents.push(mouse_5);
    guiltyComponents.push(polygon_3);
    guiltyComponents.push(text_5);
    
    for (const thisComponent of guiltyComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function guiltyRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'guilty' ---
    // get current time
    t = guiltyClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_13* updates
    if (t >= 0.0 && text_13.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_13.tStart = t;  // (not accounting for frame time here)
      text_13.frameNStart = frameN;  // exact frame index
      
      text_13.setAutoDraw(true);
    }
    
    
    // *slider_3* updates
    if (t >= 0.0 && slider_3.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_3.tStart = t;  // (not accounting for frame time here)
      slider_3.frameNStart = frameN;  // exact frame index
      
      slider_3.setAutoDraw(true);
    }
    
    
    // *polygon_5* updates
    if (t >= 0.0 && polygon_5.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_5.tStart = t;  // (not accounting for frame time here)
      polygon_5.frameNStart = frameN;  // exact frame index
      
      polygon_5.setAutoDraw(true);
    }
    
    
    // *text_17* updates
    if (t >= 0.0 && text_17.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_17.tStart = t;  // (not accounting for frame time here)
      text_17.frameNStart = frameN;  // exact frame index
      
      text_17.setAutoDraw(true);
    }
    
    // *mouse_5* updates
    if (t >= 0.0 && mouse_5.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_5.tStart = t;  // (not accounting for frame time here)
      mouse_5.frameNStart = frameN;  // exact frame index
      
      mouse_5.status = PsychoJS.Status.STARTED;
      mouse_5.mouseClock.reset();
      prevButtonState = mouse_5.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_5.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_5.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_5)) {
              gotValidClick = true;
              mouse_5.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_5.getPos();
          mouse_5.x.push(_mouseXYs[0]);
          mouse_5.y.push(_mouseXYs[1]);
          mouse_5.leftButton.push(_mouseButtons[0]);
          mouse_5.midButton.push(_mouseButtons[1]);
          mouse_5.rightButton.push(_mouseButtons[2]);
          mouse_5.time.push(mouse_5.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon_3* updates
    if (t >= 0.0 && polygon_3.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_3.tStart = t;  // (not accounting for frame time here)
      polygon_3.frameNStart = frameN;  // exact frame index
      
      polygon_3.setAutoDraw(true);
    }
    
    
    // *text_5* updates
    if (t >= 0.0 && text_5.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_5.tStart = t;  // (not accounting for frame time here)
      text_5.frameNStart = frameN;  // exact frame index
      
      text_5.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of guiltyComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function guiltyRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'guilty' ---
    for (const thisComponent of guiltyComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('guilty.stopped', globalClock.getTime());
    psychoJS.window.color = guiltyStartWinParams['color'];
    psychoJS.window.colorSpace = guiltyStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = guiltyStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = guiltyStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_3.response', slider_3.getRating());
    psychoJS.experiment.addData('slider_3.rt', slider_3.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_5.x) {  psychoJS.experiment.addData('mouse_5.x', mouse_5.x[0])};
    if (mouse_5.y) {  psychoJS.experiment.addData('mouse_5.y', mouse_5.y[0])};
    if (mouse_5.leftButton) {  psychoJS.experiment.addData('mouse_5.leftButton', mouse_5.leftButton[0])};
    if (mouse_5.midButton) {  psychoJS.experiment.addData('mouse_5.midButton', mouse_5.midButton[0])};
    if (mouse_5.rightButton) {  psychoJS.experiment.addData('mouse_5.rightButton', mouse_5.rightButton[0])};
    if (mouse_5.time) {  psychoJS.experiment.addData('mouse_5.time', mouse_5.time[0])};
    if (mouse_5.clicked_name) {  psychoJS.experiment.addData('mouse_5.clicked_name', mouse_5.clicked_name[0])};
    
    // the Routine "guilty" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var endsmeansStartWinParams;
var endsmeansComponents;
function endsmeansRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'endsmeans' ---
    t = 0;
    endsmeansClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('endsmeans.started', globalClock.getTime());
    endsmeansStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_4.reset()
    // setup some python lists for storing info about the mouse_6
    // current position of the mouse:
    mouse_6.x = [];
    mouse_6.y = [];
    mouse_6.leftButton = [];
    mouse_6.midButton = [];
    mouse_6.rightButton = [];
    mouse_6.time = [];
    mouse_6.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    endsmeansComponents = [];
    endsmeansComponents.push(text_14);
    endsmeansComponents.push(slider_4);
    endsmeansComponents.push(polygon_6);
    endsmeansComponents.push(text_18);
    endsmeansComponents.push(mouse_6);
    endsmeansComponents.push(polygon_7);
    endsmeansComponents.push(text_6);
    
    for (const thisComponent of endsmeansComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function endsmeansRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'endsmeans' ---
    // get current time
    t = endsmeansClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_14* updates
    if (t >= 0.0 && text_14.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_14.tStart = t;  // (not accounting for frame time here)
      text_14.frameNStart = frameN;  // exact frame index
      
      text_14.setAutoDraw(true);
    }
    
    
    // *slider_4* updates
    if (t >= 0.0 && slider_4.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_4.tStart = t;  // (not accounting for frame time here)
      slider_4.frameNStart = frameN;  // exact frame index
      
      slider_4.setAutoDraw(true);
    }
    
    
    // *polygon_6* updates
    if (t >= 0.0 && polygon_6.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_6.tStart = t;  // (not accounting for frame time here)
      polygon_6.frameNStart = frameN;  // exact frame index
      
      polygon_6.setAutoDraw(true);
    }
    
    
    // *text_18* updates
    if (t >= 0.0 && text_18.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_18.tStart = t;  // (not accounting for frame time here)
      text_18.frameNStart = frameN;  // exact frame index
      
      text_18.setAutoDraw(true);
    }
    
    // *mouse_6* updates
    if (t >= 0.0 && mouse_6.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_6.tStart = t;  // (not accounting for frame time here)
      mouse_6.frameNStart = frameN;  // exact frame index
      
      mouse_6.status = PsychoJS.Status.STARTED;
      mouse_6.mouseClock.reset();
      prevButtonState = mouse_6.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_6.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_6.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_6)) {
              gotValidClick = true;
              mouse_6.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_6.getPos();
          mouse_6.x.push(_mouseXYs[0]);
          mouse_6.y.push(_mouseXYs[1]);
          mouse_6.leftButton.push(_mouseButtons[0]);
          mouse_6.midButton.push(_mouseButtons[1]);
          mouse_6.rightButton.push(_mouseButtons[2]);
          mouse_6.time.push(mouse_6.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon_7* updates
    if (t >= 0.0 && polygon_7.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_7.tStart = t;  // (not accounting for frame time here)
      polygon_7.frameNStart = frameN;  // exact frame index
      
      polygon_7.setAutoDraw(true);
    }
    
    
    // *text_6* updates
    if (t >= 0.0 && text_6.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_6.tStart = t;  // (not accounting for frame time here)
      text_6.frameNStart = frameN;  // exact frame index
      
      text_6.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of endsmeansComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function endsmeansRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'endsmeans' ---
    for (const thisComponent of endsmeansComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('endsmeans.stopped', globalClock.getTime());
    psychoJS.window.color = endsmeansStartWinParams['color'];
    psychoJS.window.colorSpace = endsmeansStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = endsmeansStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = endsmeansStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_4.response', slider_4.getRating());
    psychoJS.experiment.addData('slider_4.rt', slider_4.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_6.x) {  psychoJS.experiment.addData('mouse_6.x', mouse_6.x[0])};
    if (mouse_6.y) {  psychoJS.experiment.addData('mouse_6.y', mouse_6.y[0])};
    if (mouse_6.leftButton) {  psychoJS.experiment.addData('mouse_6.leftButton', mouse_6.leftButton[0])};
    if (mouse_6.midButton) {  psychoJS.experiment.addData('mouse_6.midButton', mouse_6.midButton[0])};
    if (mouse_6.rightButton) {  psychoJS.experiment.addData('mouse_6.rightButton', mouse_6.rightButton[0])};
    if (mouse_6.time) {  psychoJS.experiment.addData('mouse_6.time', mouse_6.time[0])};
    if (mouse_6.clicked_name) {  psychoJS.experiment.addData('mouse_6.clicked_name', mouse_6.clicked_name[0])};
    
    // the Routine "endsmeans" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var rolereversalStartWinParams;
var rolereversalComponents;
function rolereversalRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'rolereversal' ---
    t = 0;
    rolereversalClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('rolereversal.started', globalClock.getTime());
    rolereversalStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_5.reset()
    // setup some python lists for storing info about the mouse_7
    // current position of the mouse:
    mouse_7.x = [];
    mouse_7.y = [];
    mouse_7.leftButton = [];
    mouse_7.midButton = [];
    mouse_7.rightButton = [];
    mouse_7.time = [];
    mouse_7.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    rolereversalComponents = [];
    rolereversalComponents.push(text_15);
    rolereversalComponents.push(slider_5);
    rolereversalComponents.push(polygon_8);
    rolereversalComponents.push(text_19);
    rolereversalComponents.push(mouse_7);
    rolereversalComponents.push(polygon_11);
    rolereversalComponents.push(text_20);
    
    for (const thisComponent of rolereversalComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function rolereversalRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'rolereversal' ---
    // get current time
    t = rolereversalClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_15* updates
    if (t >= 0.0 && text_15.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_15.tStart = t;  // (not accounting for frame time here)
      text_15.frameNStart = frameN;  // exact frame index
      
      text_15.setAutoDraw(true);
    }
    
    
    // *slider_5* updates
    if (t >= 0.0 && slider_5.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_5.tStart = t;  // (not accounting for frame time here)
      slider_5.frameNStart = frameN;  // exact frame index
      
      slider_5.setAutoDraw(true);
    }
    
    
    // *polygon_8* updates
    if (t >= 0.0 && polygon_8.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_8.tStart = t;  // (not accounting for frame time here)
      polygon_8.frameNStart = frameN;  // exact frame index
      
      polygon_8.setAutoDraw(true);
    }
    
    
    // *text_19* updates
    if (t >= 0.0 && text_19.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_19.tStart = t;  // (not accounting for frame time here)
      text_19.frameNStart = frameN;  // exact frame index
      
      text_19.setAutoDraw(true);
    }
    
    // *mouse_7* updates
    if (t >= 0.0 && mouse_7.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_7.tStart = t;  // (not accounting for frame time here)
      mouse_7.frameNStart = frameN;  // exact frame index
      
      mouse_7.status = PsychoJS.Status.STARTED;
      mouse_7.mouseClock.reset();
      prevButtonState = mouse_7.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_7.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_7.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_7)) {
              gotValidClick = true;
              mouse_7.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_7.getPos();
          mouse_7.x.push(_mouseXYs[0]);
          mouse_7.y.push(_mouseXYs[1]);
          mouse_7.leftButton.push(_mouseButtons[0]);
          mouse_7.midButton.push(_mouseButtons[1]);
          mouse_7.rightButton.push(_mouseButtons[2]);
          mouse_7.time.push(mouse_7.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon_11* updates
    if (t >= 0.0 && polygon_11.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_11.tStart = t;  // (not accounting for frame time here)
      polygon_11.frameNStart = frameN;  // exact frame index
      
      polygon_11.setAutoDraw(true);
    }
    
    
    // *text_20* updates
    if (t >= 0.0 && text_20.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_20.tStart = t;  // (not accounting for frame time here)
      text_20.frameNStart = frameN;  // exact frame index
      
      text_20.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of rolereversalComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function rolereversalRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'rolereversal' ---
    for (const thisComponent of rolereversalComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('rolereversal.stopped', globalClock.getTime());
    psychoJS.window.color = rolereversalStartWinParams['color'];
    psychoJS.window.colorSpace = rolereversalStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = rolereversalStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = rolereversalStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_5.response', slider_5.getRating());
    psychoJS.experiment.addData('slider_5.rt', slider_5.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_7.x) {  psychoJS.experiment.addData('mouse_7.x', mouse_7.x[0])};
    if (mouse_7.y) {  psychoJS.experiment.addData('mouse_7.y', mouse_7.y[0])};
    if (mouse_7.leftButton) {  psychoJS.experiment.addData('mouse_7.leftButton', mouse_7.leftButton[0])};
    if (mouse_7.midButton) {  psychoJS.experiment.addData('mouse_7.midButton', mouse_7.midButton[0])};
    if (mouse_7.rightButton) {  psychoJS.experiment.addData('mouse_7.rightButton', mouse_7.rightButton[0])};
    if (mouse_7.time) {  psychoJS.experiment.addData('mouse_7.time', mouse_7.time[0])};
    if (mouse_7.clicked_name) {  psychoJS.experiment.addData('mouse_7.clicked_name', mouse_7.clicked_name[0])};
    
    // the Routine "rolereversal" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var feelStartWinParams;
var feelComponents;
function feelRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'feel' ---
    t = 0;
    feelClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('feel.started', globalClock.getTime());
    feelStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_6.reset()
    // setup some python lists for storing info about the mouse_8
    // current position of the mouse:
    mouse_8.x = [];
    mouse_8.y = [];
    mouse_8.leftButton = [];
    mouse_8.midButton = [];
    mouse_8.rightButton = [];
    mouse_8.time = [];
    mouse_8.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    feelComponents = [];
    feelComponents.push(text_21);
    feelComponents.push(slider_6);
    feelComponents.push(polygon_12);
    feelComponents.push(text_22);
    feelComponents.push(mouse_8);
    feelComponents.push(polygon_13);
    feelComponents.push(text_23);
    
    for (const thisComponent of feelComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function feelRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'feel' ---
    // get current time
    t = feelClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_21* updates
    if (t >= 0.0 && text_21.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_21.tStart = t;  // (not accounting for frame time here)
      text_21.frameNStart = frameN;  // exact frame index
      
      text_21.setAutoDraw(true);
    }
    
    
    // *slider_6* updates
    if (t >= 0.0 && slider_6.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_6.tStart = t;  // (not accounting for frame time here)
      slider_6.frameNStart = frameN;  // exact frame index
      
      slider_6.setAutoDraw(true);
    }
    
    
    // *polygon_12* updates
    if (t >= 0.0 && polygon_12.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_12.tStart = t;  // (not accounting for frame time here)
      polygon_12.frameNStart = frameN;  // exact frame index
      
      polygon_12.setAutoDraw(true);
    }
    
    
    // *text_22* updates
    if (t >= 0.0 && text_22.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_22.tStart = t;  // (not accounting for frame time here)
      text_22.frameNStart = frameN;  // exact frame index
      
      text_22.setAutoDraw(true);
    }
    
    // *mouse_8* updates
    if (t >= 0.0 && mouse_8.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_8.tStart = t;  // (not accounting for frame time here)
      mouse_8.frameNStart = frameN;  // exact frame index
      
      mouse_8.status = PsychoJS.Status.STARTED;
      mouse_8.mouseClock.reset();
      prevButtonState = mouse_8.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_8.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_8.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_8)) {
              gotValidClick = true;
              mouse_8.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_8.getPos();
          mouse_8.x.push(_mouseXYs[0]);
          mouse_8.y.push(_mouseXYs[1]);
          mouse_8.leftButton.push(_mouseButtons[0]);
          mouse_8.midButton.push(_mouseButtons[1]);
          mouse_8.rightButton.push(_mouseButtons[2]);
          mouse_8.time.push(mouse_8.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon_13* updates
    if (t >= 0.0 && polygon_13.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_13.tStart = t;  // (not accounting for frame time here)
      polygon_13.frameNStart = frameN;  // exact frame index
      
      polygon_13.setAutoDraw(true);
    }
    
    
    // *text_23* updates
    if (t >= 0.0 && text_23.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_23.tStart = t;  // (not accounting for frame time here)
      text_23.frameNStart = frameN;  // exact frame index
      
      text_23.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of feelComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function feelRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'feel' ---
    for (const thisComponent of feelComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('feel.stopped', globalClock.getTime());
    psychoJS.window.color = feelStartWinParams['color'];
    psychoJS.window.colorSpace = feelStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = feelStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = feelStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_6.response', slider_6.getRating());
    psychoJS.experiment.addData('slider_6.rt', slider_6.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_8.x) {  psychoJS.experiment.addData('mouse_8.x', mouse_8.x[0])};
    if (mouse_8.y) {  psychoJS.experiment.addData('mouse_8.y', mouse_8.y[0])};
    if (mouse_8.leftButton) {  psychoJS.experiment.addData('mouse_8.leftButton', mouse_8.leftButton[0])};
    if (mouse_8.midButton) {  psychoJS.experiment.addData('mouse_8.midButton', mouse_8.midButton[0])};
    if (mouse_8.rightButton) {  psychoJS.experiment.addData('mouse_8.rightButton', mouse_8.rightButton[0])};
    if (mouse_8.time) {  psychoJS.experiment.addData('mouse_8.time', mouse_8.time[0])};
    if (mouse_8.clicked_name) {  psychoJS.experiment.addData('mouse_8.clicked_name', mouse_8.clicked_name[0])};
    
    // the Routine "feel" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var questions_physStartWinParams;
var _key_resp_7_allKeys;
var questions_physComponents;
function questions_physRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'questions_phys' ---
    t = 0;
    questions_physClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('questions_phys.started', globalClock.getTime());
    questions_physStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_7.keys = undefined;
    key_resp_7.rt = undefined;
    _key_resp_7_allKeys = [];
    // keep track of which components have finished
    questions_physComponents = [];
    questions_physComponents.push(text_58);
    questions_physComponents.push(key_resp_7);
    
    for (const thisComponent of questions_physComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function questions_physRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'questions_phys' ---
    // get current time
    t = questions_physClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_58* updates
    if (t >= 0.0 && text_58.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_58.tStart = t;  // (not accounting for frame time here)
      text_58.frameNStart = frameN;  // exact frame index
      
      text_58.setAutoDraw(true);
    }
    
    
    // *key_resp_7* updates
    if (t >= 0.0 && key_resp_7.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_7.tStart = t;  // (not accounting for frame time here)
      key_resp_7.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_7.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_7.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_7.clearEvents(); });
    }
    
    if (key_resp_7.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_7.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_7_allKeys = _key_resp_7_allKeys.concat(theseKeys);
      if (_key_resp_7_allKeys.length > 0) {
        key_resp_7.keys = _key_resp_7_allKeys[_key_resp_7_allKeys.length - 1].name;  // just the last key pressed
        key_resp_7.rt = _key_resp_7_allKeys[_key_resp_7_allKeys.length - 1].rt;
        key_resp_7.duration = _key_resp_7_allKeys[_key_resp_7_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of questions_physComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function questions_physRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'questions_phys' ---
    for (const thisComponent of questions_physComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('questions_phys.stopped', globalClock.getTime());
    psychoJS.window.color = questions_physStartWinParams['color'];
    psychoJS.window.colorSpace = questions_physStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = questions_physStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = questions_physStartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_7.corr, level);
    }
    psychoJS.experiment.addData('key_resp_7.keys', key_resp_7.keys);
    if (typeof key_resp_7.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_7.rt', key_resp_7.rt);
        psychoJS.experiment.addData('key_resp_7.duration', key_resp_7.duration);
        routineTimer.reset();
        }
    
    key_resp_7.stop();
    // the Routine "questions_phys" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var look2StartWinParams;
var look2Components;
function look2RoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'look2' ---
    t = 0;
    look2Clock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('look2.started', globalClock.getTime());
    look2StartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_7.reset()
    // setup some python lists for storing info about the mouse_9
    // current position of the mouse:
    mouse_9.x = [];
    mouse_9.y = [];
    mouse_9.leftButton = [];
    mouse_9.midButton = [];
    mouse_9.rightButton = [];
    mouse_9.time = [];
    mouse_9.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    look2Components = [];
    look2Components.push(text_28);
    look2Components.push(slider_7);
    look2Components.push(polygon_15);
    look2Components.push(text_31);
    look2Components.push(mouse_9);
    look2Components.push(polygon_16);
    look2Components.push(text_32);
    look2Components.push(text_33);
    look2Components.push(text_35);
    
    for (const thisComponent of look2Components)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function look2RoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'look2' ---
    // get current time
    t = look2Clock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_28* updates
    if (t >= 0.0 && text_28.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_28.tStart = t;  // (not accounting for frame time here)
      text_28.frameNStart = frameN;  // exact frame index
      
      text_28.setAutoDraw(true);
    }
    
    
    // *slider_7* updates
    if (t >= 0.0 && slider_7.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_7.tStart = t;  // (not accounting for frame time here)
      slider_7.frameNStart = frameN;  // exact frame index
      
      slider_7.setAutoDraw(true);
    }
    
    
    // *polygon_15* updates
    if (t >= 0.0 && polygon_15.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_15.tStart = t;  // (not accounting for frame time here)
      polygon_15.frameNStart = frameN;  // exact frame index
      
      polygon_15.setAutoDraw(true);
    }
    
    
    // *text_31* updates
    if (t >= 0.0 && text_31.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_31.tStart = t;  // (not accounting for frame time here)
      text_31.frameNStart = frameN;  // exact frame index
      
      text_31.setAutoDraw(true);
    }
    
    // *mouse_9* updates
    if (t >= 0.0 && mouse_9.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_9.tStart = t;  // (not accounting for frame time here)
      mouse_9.frameNStart = frameN;  // exact frame index
      
      mouse_9.status = PsychoJS.Status.STARTED;
      mouse_9.mouseClock.reset();
      prevButtonState = mouse_9.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_9.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_9.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_9)) {
              gotValidClick = true;
              mouse_9.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_9.getPos();
          mouse_9.x.push(_mouseXYs[0]);
          mouse_9.y.push(_mouseXYs[1]);
          mouse_9.leftButton.push(_mouseButtons[0]);
          mouse_9.midButton.push(_mouseButtons[1]);
          mouse_9.rightButton.push(_mouseButtons[2]);
          mouse_9.time.push(mouse_9.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon_16* updates
    if (t >= 0.0 && polygon_16.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_16.tStart = t;  // (not accounting for frame time here)
      polygon_16.frameNStart = frameN;  // exact frame index
      
      polygon_16.setAutoDraw(true);
    }
    
    
    // *text_32* updates
    if (t >= 0.0 && text_32.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_32.tStart = t;  // (not accounting for frame time here)
      text_32.frameNStart = frameN;  // exact frame index
      
      text_32.setAutoDraw(true);
    }
    
    
    // *text_33* updates
    if (t >= 0.0 && text_33.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_33.tStart = t;  // (not accounting for frame time here)
      text_33.frameNStart = frameN;  // exact frame index
      
      text_33.setAutoDraw(true);
    }
    
    
    // *text_35* updates
    if (t >= 0.0 && text_35.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_35.tStart = t;  // (not accounting for frame time here)
      text_35.frameNStart = frameN;  // exact frame index
      
      text_35.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of look2Components)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function look2RoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'look2' ---
    for (const thisComponent of look2Components) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('look2.stopped', globalClock.getTime());
    psychoJS.window.color = look2StartWinParams['color'];
    psychoJS.window.colorSpace = look2StartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = look2StartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = look2StartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_7.response', slider_7.getRating());
    psychoJS.experiment.addData('slider_7.rt', slider_7.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_9.x) {  psychoJS.experiment.addData('mouse_9.x', mouse_9.x[0])};
    if (mouse_9.y) {  psychoJS.experiment.addData('mouse_9.y', mouse_9.y[0])};
    if (mouse_9.leftButton) {  psychoJS.experiment.addData('mouse_9.leftButton', mouse_9.leftButton[0])};
    if (mouse_9.midButton) {  psychoJS.experiment.addData('mouse_9.midButton', mouse_9.midButton[0])};
    if (mouse_9.rightButton) {  psychoJS.experiment.addData('mouse_9.rightButton', mouse_9.rightButton[0])};
    if (mouse_9.time) {  psychoJS.experiment.addData('mouse_9.time', mouse_9.time[0])};
    if (mouse_9.clicked_name) {  psychoJS.experiment.addData('mouse_9.clicked_name', mouse_9.clicked_name[0])};
    
    // the Routine "look2" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var trustStartWinParams;
var trustComponents;
function trustRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'trust' ---
    t = 0;
    trustClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('trust.started', globalClock.getTime());
    trustStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    slider_8.reset()
    // setup some python lists for storing info about the mouse_10
    // current position of the mouse:
    mouse_10.x = [];
    mouse_10.y = [];
    mouse_10.leftButton = [];
    mouse_10.midButton = [];
    mouse_10.rightButton = [];
    mouse_10.time = [];
    mouse_10.clicked_name = [];
    gotValidClick = false; // until a click is received
    // keep track of which components have finished
    trustComponents = [];
    trustComponents.push(text_52);
    trustComponents.push(slider_8);
    trustComponents.push(polygon_17);
    trustComponents.push(text_53);
    trustComponents.push(mouse_10);
    trustComponents.push(polygon_18);
    trustComponents.push(text_54);
    trustComponents.push(text_55);
    trustComponents.push(text_56);
    
    for (const thisComponent of trustComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function trustRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'trust' ---
    // get current time
    t = trustClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_52* updates
    if (t >= 0.0 && text_52.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_52.tStart = t;  // (not accounting for frame time here)
      text_52.frameNStart = frameN;  // exact frame index
      
      text_52.setAutoDraw(true);
    }
    
    
    // *slider_8* updates
    if (t >= 0.0 && slider_8.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      slider_8.tStart = t;  // (not accounting for frame time here)
      slider_8.frameNStart = frameN;  // exact frame index
      
      slider_8.setAutoDraw(true);
    }
    
    
    // *polygon_17* updates
    if (t >= 0.0 && polygon_17.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_17.tStart = t;  // (not accounting for frame time here)
      polygon_17.frameNStart = frameN;  // exact frame index
      
      polygon_17.setAutoDraw(true);
    }
    
    
    // *text_53* updates
    if (t >= 0.0 && text_53.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_53.tStart = t;  // (not accounting for frame time here)
      text_53.frameNStart = frameN;  // exact frame index
      
      text_53.setAutoDraw(true);
    }
    
    // *mouse_10* updates
    if (t >= 0.0 && mouse_10.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      mouse_10.tStart = t;  // (not accounting for frame time here)
      mouse_10.frameNStart = frameN;  // exact frame index
      
      mouse_10.status = PsychoJS.Status.STARTED;
      mouse_10.mouseClock.reset();
      prevButtonState = mouse_10.getPressed();  // if button is down already this ISN'T a new click
      }
    if (mouse_10.status === PsychoJS.Status.STARTED) {  // only update if started and not finished!
      _mouseButtons = mouse_10.getPressed();
      if (!_mouseButtons.every( (e,i,) => (e == prevButtonState[i]) )) { // button state changed?
        prevButtonState = _mouseButtons;
        if (_mouseButtons.reduce( (e, acc) => (e+acc) ) > 0) { // state changed to a new click
          // check if the mouse was inside our 'clickable' objects
          gotValidClick = false;
          for (const obj of [polygon_4]) {
            if (obj.contains(mouse_10)) {
              gotValidClick = true;
              mouse_10.clicked_name.push(obj.name)
            }
          }
          _mouseXYs = mouse_10.getPos();
          mouse_10.x.push(_mouseXYs[0]);
          mouse_10.y.push(_mouseXYs[1]);
          mouse_10.leftButton.push(_mouseButtons[0]);
          mouse_10.midButton.push(_mouseButtons[1]);
          mouse_10.rightButton.push(_mouseButtons[2]);
          mouse_10.time.push(mouse_10.mouseClock.getTime());
          if (gotValidClick === true) { // end routine on response
            continueRoutine = false;
          }
        }
      }
    }
    
    // *polygon_18* updates
    if (t >= 0.0 && polygon_18.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      polygon_18.tStart = t;  // (not accounting for frame time here)
      polygon_18.frameNStart = frameN;  // exact frame index
      
      polygon_18.setAutoDraw(true);
    }
    
    
    // *text_54* updates
    if (t >= 0.0 && text_54.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_54.tStart = t;  // (not accounting for frame time here)
      text_54.frameNStart = frameN;  // exact frame index
      
      text_54.setAutoDraw(true);
    }
    
    
    // *text_55* updates
    if (t >= 0.0 && text_55.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_55.tStart = t;  // (not accounting for frame time here)
      text_55.frameNStart = frameN;  // exact frame index
      
      text_55.setAutoDraw(true);
    }
    
    
    // *text_56* updates
    if (t >= 0.0 && text_56.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_56.tStart = t;  // (not accounting for frame time here)
      text_56.frameNStart = frameN;  // exact frame index
      
      text_56.setAutoDraw(true);
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of trustComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function trustRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'trust' ---
    for (const thisComponent of trustComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('trust.stopped', globalClock.getTime());
    psychoJS.window.color = trustStartWinParams['color'];
    psychoJS.window.colorSpace = trustStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = trustStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = trustStartWinParams['backgroundFit'];
    psychoJS.experiment.addData('slider_8.response', slider_8.getRating());
    psychoJS.experiment.addData('slider_8.rt', slider_8.getRT());
    // store data for psychoJS.experiment (ExperimentHandler)
    if (mouse_10.x) {  psychoJS.experiment.addData('mouse_10.x', mouse_10.x[0])};
    if (mouse_10.y) {  psychoJS.experiment.addData('mouse_10.y', mouse_10.y[0])};
    if (mouse_10.leftButton) {  psychoJS.experiment.addData('mouse_10.leftButton', mouse_10.leftButton[0])};
    if (mouse_10.midButton) {  psychoJS.experiment.addData('mouse_10.midButton', mouse_10.midButton[0])};
    if (mouse_10.rightButton) {  psychoJS.experiment.addData('mouse_10.rightButton', mouse_10.rightButton[0])};
    if (mouse_10.time) {  psychoJS.experiment.addData('mouse_10.time', mouse_10.time[0])};
    if (mouse_10.clicked_name) {  psychoJS.experiment.addData('mouse_10.clicked_name', mouse_10.clicked_name[0])};
    
    // the Routine "trust" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var endofroundStartWinParams;
var endofroundComponents;
function endofroundRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'endofround' ---
    t = 0;
    endofroundClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    routineTimer.add(5.000000);
    // update component parameters for each repeat
    psychoJS.experiment.addData('endofround.started', globalClock.getTime());
    endofroundStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    sound_4.secs=1.0;
    sound_4.setVolume(1.0);
    // keep track of which components have finished
    endofroundComponents = [];
    endofroundComponents.push(text_51);
    endofroundComponents.push(sound_4);
    
    for (const thisComponent of endofroundComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function endofroundRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'endofround' ---
    // get current time
    t = endofroundClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_51* updates
    if (t >= 0.0 && text_51.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_51.tStart = t;  // (not accounting for frame time here)
      text_51.frameNStart = frameN;  // exact frame index
      
      text_51.setAutoDraw(true);
    }
    
    frameRemains = 0.0 + 5 - psychoJS.window.monitorFramePeriod * 0.75;  // most of one frame period left
    if (text_51.status === PsychoJS.Status.STARTED && t >= frameRemains) {
      text_51.setAutoDraw(false);
    }
    // start/stop sound_4
    if (t >= 0.0 && sound_4.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      sound_4.tStart = t;  // (not accounting for frame time here)
      sound_4.frameNStart = frameN;  // exact frame index
      
      psychoJS.window.callOnFlip(function(){ sound_4.play(); });  // screen flip
      sound_4.status = PsychoJS.Status.STARTED;
    }
    frameRemains = 0.0 + 1.0 - psychoJS.window.monitorFramePeriod * 0.75;  // most of one frame period left
    if (sound_4.status === PsychoJS.Status.STARTED && t >= frameRemains) {
      if (t >= sound_4.tStart + 0.5) {
        sound_4.stop();  // stop the sound (if longer than duration)
        sound_4.status = PsychoJS.Status.FINISHED;
      }
    }
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of endofroundComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine && routineTimer.getTime() > 0) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function endofroundRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'endofround' ---
    for (const thisComponent of endofroundComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('endofround.stopped', globalClock.getTime());
    psychoJS.window.color = endofroundStartWinParams['color'];
    psychoJS.window.colorSpace = endofroundStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = endofroundStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = endofroundStartWinParams['backgroundFit'];
    sound_4.stop();  // ensure sound has stopped at end of Routine
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


var EndStartWinParams;
var _key_resp_2_allKeys;
var EndComponents;
function EndRoutineBegin(snapshot) {
  return async function () {
    TrialHandler.fromSnapshot(snapshot); // ensure that .thisN vals are up to date
    
    //--- Prepare to start Routine 'End' ---
    t = 0;
    EndClock.reset(); // clock
    frameN = -1;
    continueRoutine = true; // until we're told otherwise
    // update component parameters for each repeat
    psychoJS.experiment.addData('End.started', globalClock.getTime());
    EndStartWinParams = {
        'color': psychoJS.window.color,
        'colorSpace': psychoJS.window.colorSpace,
        'backgroundImage': psychoJS.window.backgroundImage,
        'backgroundFit': psychoJS.window.backgroundFit,
    };
    psychoJS.window.color = 'black';
    psychoJS.window.colorSpace = 'rgb';
    psychoJS.window.backgroundImage = '';
    psychoJS.window.backgroundFit = 'none';
    key_resp_2.keys = undefined;
    key_resp_2.rt = undefined;
    _key_resp_2_allKeys = [];
    // keep track of which components have finished
    EndComponents = [];
    EndComponents.push(text_4);
    EndComponents.push(key_resp_2);
    
    for (const thisComponent of EndComponents)
      if ('status' in thisComponent)
        thisComponent.status = PsychoJS.Status.NOT_STARTED;
    return Scheduler.Event.NEXT;
  }
}


function EndRoutineEachFrame() {
  return async function () {
    //--- Loop for each frame of Routine 'End' ---
    // get current time
    t = EndClock.getTime();
    frameN = frameN + 1;// number of completed frames (so 0 is the first frame)
    // update/draw components on each frame
    
    // *text_4* updates
    if (t >= 0.0 && text_4.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      text_4.tStart = t;  // (not accounting for frame time here)
      text_4.frameNStart = frameN;  // exact frame index
      
      text_4.setAutoDraw(true);
    }
    
    
    // *key_resp_2* updates
    if (t >= 0.0 && key_resp_2.status === PsychoJS.Status.NOT_STARTED) {
      // keep track of start time/frame for later
      key_resp_2.tStart = t;  // (not accounting for frame time here)
      key_resp_2.frameNStart = frameN;  // exact frame index
      
      // keyboard checking is just starting
      psychoJS.window.callOnFlip(function() { key_resp_2.clock.reset(); });  // t=0 on next screen flip
      psychoJS.window.callOnFlip(function() { key_resp_2.start(); }); // start on screen flip
      psychoJS.window.callOnFlip(function() { key_resp_2.clearEvents(); });
    }
    
    if (key_resp_2.status === PsychoJS.Status.STARTED) {
      let theseKeys = key_resp_2.getKeys({keyList: ['space'], waitRelease: false});
      _key_resp_2_allKeys = _key_resp_2_allKeys.concat(theseKeys);
      if (_key_resp_2_allKeys.length > 0) {
        key_resp_2.keys = _key_resp_2_allKeys[_key_resp_2_allKeys.length - 1].name;  // just the last key pressed
        key_resp_2.rt = _key_resp_2_allKeys[_key_resp_2_allKeys.length - 1].rt;
        key_resp_2.duration = _key_resp_2_allKeys[_key_resp_2_allKeys.length - 1].duration;
        // a response ends the routine
        continueRoutine = false;
      }
    }
    
    // check for quit (typically the Esc key)
    if (psychoJS.experiment.experimentEnded || psychoJS.eventManager.getKeys({keyList:['escape']}).length > 0) {
      return quitPsychoJS('The [Escape] key was pressed. Goodbye!', false);
    }
    
    // check if the Routine should terminate
    if (!continueRoutine) {  // a component has requested a forced-end of Routine
      return Scheduler.Event.NEXT;
    }
    
    continueRoutine = false;  // reverts to True if at least one component still running
    for (const thisComponent of EndComponents)
      if ('status' in thisComponent && thisComponent.status !== PsychoJS.Status.FINISHED) {
        continueRoutine = true;
        break;
      }
    
    // refresh the screen if continuing
    if (continueRoutine) {
      return Scheduler.Event.FLIP_REPEAT;
    } else {
      return Scheduler.Event.NEXT;
    }
  };
}


function EndRoutineEnd(snapshot) {
  return async function () {
    //--- Ending Routine 'End' ---
    for (const thisComponent of EndComponents) {
      if (typeof thisComponent.setAutoDraw === 'function') {
        thisComponent.setAutoDraw(false);
      }
    }
    psychoJS.experiment.addData('End.stopped', globalClock.getTime());
    psychoJS.window.color = EndStartWinParams['color'];
    psychoJS.window.colorSpace = EndStartWinParams['colorSpace'];
    psychoJS.window.backgroundImage = EndStartWinParams['backgroundImage'];
    psychoJS.window.backgroundFit = EndStartWinParams['backgroundFit'];
    // update the trial handler
    if (currentLoop instanceof MultiStairHandler) {
      currentLoop.addResponse(key_resp_2.corr, level);
    }
    psychoJS.experiment.addData('key_resp_2.keys', key_resp_2.keys);
    if (typeof key_resp_2.keys !== 'undefined') {  // we had a response
        psychoJS.experiment.addData('key_resp_2.rt', key_resp_2.rt);
        psychoJS.experiment.addData('key_resp_2.duration', key_resp_2.duration);
        routineTimer.reset();
        }
    
    key_resp_2.stop();
    // the Routine "End" was not non-slip safe, so reset the non-slip timer
    routineTimer.reset();
    
    // Routines running outside a loop should always advance the datafile row
    if (currentLoop === psychoJS.experiment) {
      psychoJS.experiment.nextEntry(snapshot);
    }
    return Scheduler.Event.NEXT;
  }
}


function importConditions(currentLoop) {
  return async function () {
    psychoJS.importAttributes(currentLoop.getCurrentTrial());
    return Scheduler.Event.NEXT;
    };
}


async function quitPsychoJS(message, isCompleted) {
  // Check for and save orphaned data
  if (psychoJS.experiment.isEntryEmpty()) {
    psychoJS.experiment.nextEntry();
  }
  
  
  
  
  
  
  
  
  
  
  
  
  psychoJS.window.close();
  psychoJS.quit({message: message, isCompleted: isCompleted});
  
  return Scheduler.Event.QUIT;
}
